# Byteplant Email Validator: Native API Reference

A consolidated summary of Byteplant Email Validator's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.byteplant.com/email-validator/api.html
- **API base URL:** `https://api.email-validator.net`

## Authentication

### API Key

Authenticate with your Byteplant Email Validator API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.byteplant.com/email-validator/api.html)

## API conventions

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Email Validation Task](actions/create-bulk-email-validation-task.md) | `POST /api/bulk-verify` | [docs](https://www.byteplant.com/email-validator/api.html#bulk-api) |
| [Verify Email Address](actions/verify-email-address.md) | `GET /api/verify` | [docs](https://www.byteplant.com/email-validator/api.html#email-validation-api) |
