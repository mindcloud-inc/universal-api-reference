# WhatsApp Number Validator: Native API Reference

A consolidated summary of WhatsApp Number Validator's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://zylalabs.com/api-marketplace/communication%2B%26%2Bmessaging/whatsapp%2Bnumber%2Bvalidator%2Bapi/9470
- **API base URL:** `https://zylalabs.com/api/9470/whatsapp+number+validator+api/21752`

## Authentication

### API Key

Use your Zyla Labs API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://zylalabs.com/api-marketplace/communication%2B%26%2Bmessaging/whatsapp%2Bnumber%2Bvalidator%2Bapi/9470)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Validate WhatsApp Number](actions/validate-whats-app-number.md) | `GET number+check` | [docs](https://zylalabs.com/api-marketplace/communication%2B%26%2Bmessaging/whatsapp%2Bnumber%2Bvalidator%2Bapi/9470) |
