# SMSVio: Native API Reference

A consolidated summary of SMSVio's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.smsvio.cz/api/
- **API base URL:** `https://gate.smsvio.cz`

## Authentication

### API Key

API key authentication for SMSVio

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.smsvio.cz/api/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete SMS](actions/delete-sms.md) | `POST /services/send/` | [docs](https://www.smsvio.cz/api/) |
| [Get Account Credits](actions/get-account-credits.md) | `POST /services/send/` | [docs](https://www.smsvio.cz/api/) |
| [Get SMS Details](actions/get-sms-details.md) | `POST /services/send/` | [docs](https://www.smsvio.cz/api/) |
| [Send SMS](actions/send-sms.md) | `POST /services/send/` | [docs](https://www.smsvio.cz/api/) |
| [Send SMS to Multiple Numbers](actions/send-sms-to-multiple-numbers.md) | `POST /services/send/` | [docs](https://www.smsvio.cz/api/) |
