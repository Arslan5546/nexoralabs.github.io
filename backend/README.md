# Nexora Ventures backend blueprint

This directory documents the production backend contract. GitHub Pages remains a static demo only.

## API modules
- `auth`: register, login, email verification, password reset, 2FA
- `users`: profile and account status
- `kyc`: submit/review identity verification
- `projects`: venture discovery and project details
- `investments`: eligibility, orders, holdings and distributions
- `transactions`: immutable payment/ledger records and provider webhooks
- `documents`: private investor documents
- `notifications`: user alerts
- `admin`: RBAC-protected operations
- `reports`: financial and portfolio reporting

## Suggested stack
Node.js/NestJS + PostgreSQL + private object storage + managed secrets + a regulated/approved payment provider.

## Security requirements
Never store passwords, API keys, payment credentials, CNIC/passport files, or admin secrets in this GitHub Pages repository. Use Argon2/bcrypt password hashing, secure HTTP-only sessions, CSRF protection, rate limiting, 2FA for privileged users, encryption at rest, webhook signature validation, least-privilege RBAC and audit logs.

## Production boundary
No real-money deposits, withdrawals, guaranteed returns, or investment solicitation are implemented by this static repository. Any regulated investment functionality must be added only after the applicable legal/licensing/compliance review.