
# Project 01 — AWS Account Hardening

## Objective
Secure a brand new AWS account following security best practices
before doing any lab work.

## What I Did

### 1. Root Account Protection
- Enabled MFA on root account using Google Authenticator
- Never use root for daily tasks — principle of least privilege

### 2. IAM Admin User Created
- Created IAM user: rajesh-admin
- Attached policy: AdministratorAccess
- Enabled Console + Programmatic access
- Saved credentials CSV securely (never committed to GitHub)

### 3. Billing Protection
- Created $5 budget alert via AWS Budgets
- Alert triggers at 80% threshold → email notification

### 4. CloudTrail Verified
- Confirmed Event History is logging all API calls
- Verified my own CreateUser and CreateKeyPair events are visible

## Security Concepts Applied
| Concept | How Applied |
|---------|-------------|
| Least Privilege | Root account locked down, IAM user for daily use |
| MFA / 2FA | Enabled on root — blocks 99% of account takeover attacks |
| Audit Logging | CloudTrail capturing all API activity |
| Cost Control | Billing alert prevents surprise charges |

## Screenshot
![AWS IAM Dashboard](screenshots/iam-dashboard.png)
![MFA Enabled](screenshots/mfa-enabled.png)

## Key Learning
This mirrors what I do in enterprise VM work — before scanning
or remediating vulnerabilities, you first harden the baseline.
Same principle applies to a new AWS account.
