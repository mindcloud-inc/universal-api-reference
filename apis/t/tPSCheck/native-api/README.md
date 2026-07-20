# TPSCheck: Native API Reference

A consolidated summary of TPSCheck's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.tpscheck.uk/documentation/
- **API base URL:** `https://api.tpscheck.uk`

## Authentication

### API key

Authenticate TPSCheck API requests with your TPSCheck API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.tpscheck.uk/documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch check phone numbers](actions/batch-check-phone-numbers.md) | `POST /batch` | [docs](https://www.tpscheck.uk/documentation/) |
| [Check phone number](actions/check-phone-number.md) | `POST /check` | [docs](https://www.tpscheck.uk/documentation/) |
| [Check status](actions/check-status.md) | `GET /status` | [docs](https://www.tpscheck.uk/documentation/) |
| [Get credits](actions/get-credits.md) | `GET /credits` | [docs](https://www.tpscheck.uk/documentation/) |
