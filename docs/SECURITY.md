# Public Repository Security Policy

This repository is an intentionally limited public export for AnimalHack 2026.

## Rules

Never commit:

- API keys, access tokens, passwords, private keys, or `.env` files
- production credentials or deployment secrets
- private infrastructure configuration
- internal-only CAIOS documentation
- proprietary source code that is not required for the public submission
- real customer, pet-owner, or identifiable pet data

## Export Model

The private CAIOS repository remains the source of truth. Material reaches this repository only after review and explicit approval for public release.

```text
PRIVATE CAIOS
    │
    │ whitelist + review
    ▼
PUBLIC ANIMALHACK REPO
```

## Synthetic Data

Demo data must be fictional or synthetic. Do not use production records to demonstrate the system.

## Before Every Public Push

1. Review changed files.
2. Check for credentials and secrets.
3. Check for personal or customer data.
4. Check that proprietary implementation details are intentionally public.
5. Confirm that documentation does not expose private infrastructure.
6. Verify the public repository contents after the push.

## Incident Response

If a secret is accidentally committed, treat it as compromised: revoke or rotate it immediately, remove it from the repository history where appropriate, and review access logs. Do not rely on deleting the visible file alone.
