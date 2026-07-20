# Super: Native API Reference

A consolidated summary of Super's API configuration, with links to official documentation.

- **Official docs:** https://developers.super.work/quickstart
- **OpenAPI specification:** https://api.super.work/openapi.json
- **API base URL:** `https://api.super.work/v1`

## Authentication

### API Key

Authenticate with a personal Super API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.super.work/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `notes`. The next-page cursor is read from `nextCursor`.
