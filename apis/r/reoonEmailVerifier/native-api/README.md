# Reoon Email Verifier: Native API Reference

A consolidated summary of Reoon Email Verifier's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/
- **API base URL:** `https://emailverifier.reoon.com/api/v1`

## Authentication

### API Key

Use your Reoon Email Verifier API key. Reoon requires the key as the `key` query parameter on each request, so this app stores one secret field and injects it directly into requests.

### Credentials

- **API Key:** `apiKey` · required · Your Reoon Email Verifier API key. MindCloud stores it once and injects it into requests as the provider-required `key` value.

[Official authentication documentation](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Account Balance](actions/check-account-balance.md) | `GET /check-account-balance/` | [docs](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/) |
| [Create Bulk Verification Task](actions/create-bulk-verification-task.md) | `POST /create-bulk-verification-task/` | [docs](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/) |
| [Get Bulk Verification Task Result](actions/get-bulk-verification-task-result.md) | `GET /get-result-bulk-verification-task/` | [docs](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/) |
| [Verify Email Power](actions/verify-email-power.md) | `GET /verify` | [docs](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/) |
| [Verify Email Quick](actions/verify-email-quick.md) | `GET /verify` | [docs](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/) |
