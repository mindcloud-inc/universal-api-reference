# ValidEmail: Native API Reference

A consolidated summary of ValidEmail's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.validemail.net/Docs/api-python
- **API base URL:** `https://api.ValidEmail.net`

## Authentication

### API Key

Connect to ValidEmail with an API key sent as the token query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.validemail.net/Docs/api-python)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | `GET /` | [docs](https://www.validemail.net/Docs/api-python) |
