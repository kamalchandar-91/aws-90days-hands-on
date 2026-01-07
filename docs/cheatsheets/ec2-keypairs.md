# EC2 Key Pairs (AWS)

## Create (RSA) and download private key (CLI)
mkdir -p ~/.ssh/aws
aws ec2 create-key-pair \
  --key-name <key-name> \
  --key-type rsa \
  --query "KeyMaterial" \
  --output text > ~/.ssh/aws/<key-name>.pem
chmod 400 ~/.ssh/aws/<key-name>.pem

## Verify
aws ec2 describe-key-pairs --key-names <key-name>

## Delete (cleanup)
aws ec2 delete-key-pair --key-name <key-name>

## Notes
- Never commit .pem files to Git.
- Ensure your AWS region is correct.
