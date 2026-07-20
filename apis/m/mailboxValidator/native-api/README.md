# MailboxValidator: Native API Reference

A consolidated summary of MailboxValidator's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.mailboxvalidator.com/web-service
- **OpenAPI specification:** https://api.mailboxvalidator.com/openapi.json
- **API base URL:** `https://api.mailboxvalidator.com`

## Authentication

### API Key

Use your MailboxValidator API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.mailboxvalidator.com/api-email-free)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Disposable Email](actions/check-disposable-email.md) | `GET /v2/email/disposable` | [docs](https://www.mailboxvalidator.com/api-email-disposable) |
| [Check Free Email Provider](actions/check-free-email-provider.md) | `GET /v2/email/free` | [docs](https://www.mailboxvalidator.com/api-email-free) |
| [Validate Email Address](actions/validate-email-address.md) | `GET /v2/validation/single` | [docs](https://www.mailboxvalidator.com/api-single-validation) |
