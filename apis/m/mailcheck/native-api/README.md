# Mailcheck: Native API Reference

A consolidated summary of Mailcheck's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://api.mailcheck.dev/docs
- **API base URL:** `https://api.mailcheck.dev`

## Authentication

### API Key

MailCheck secret API key used as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.mailcheck.dev/docs)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Verify Emails](actions/bulk-verify-emails.md) | `POST /v1/verify/bulk` | [docs](https://api.mailcheck.dev/docs#verify-bulk) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://api.mailcheck.dev/docs#account) |
| [Rotate API Key](actions/rotate-api-key.md) | `POST /v1/account/rotate-key` | [docs](https://api.mailcheck.dev/docs#rotate-key) |
| [Verify Email](actions/verify-email.md) | `POST /v1/verify` | [docs](https://api.mailcheck.dev/docs#verify) |
| [Verify Email Authenticity](actions/verify-email-authenticity.md) | `POST /v1/verify/auth` | [docs](https://api.mailcheck.dev/docs#verify-auth) |
| [Verify Raw Email Authenticity](actions/verify-raw-email-authenticity.md) | `POST /v1/verify/auth` | [docs](https://api.mailcheck.dev/docs#verify-auth) |
