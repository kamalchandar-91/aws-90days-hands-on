# Day 01 — AWS Project — Create EC2 Key Pair (RSA)

## Objective
- Create an EC2 key pair named `devops-kp` with key type `rsa`.

## Work done
- Created RSA key pair `devops-kp` in the AWS Console (KodeKloud lab).
- Confirmed the key exists.

## Commands used
```bash
# optional CLI verification (if AWS CLI is configured)
aws ec2 describe-key-pairs --key-names devops-kp
Evidence

Key pair devops-kp exists in EC2 → Key pairs.

Issues + Fix

None.

Next steps

Launch an EC2 instance using devops-kp and validate SSH access.
