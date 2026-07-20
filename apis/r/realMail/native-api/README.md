# RealMail: Native API Reference

A consolidated summary of RealMail's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.realmail.dev/docs
- **API base URL:** `https://api.realmail.dev`

## Authentication

### API Key

Use your RealMail API key. MindCloud stores it as credentials.apiKey and injects it through the shared outbound mapper.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.realmail.dev/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | `POST /v1/validate` | [docs](https://www.realmail.dev/docs) |
