# Turbot Pipes: Native API Reference

A consolidated summary of Turbot Pipes's API configuration, with links to official documentation.

- **Official docs:** https://turbot.com/pipes/docs/reference/api
- **OpenAPI specification:** https://pipes.turbot.com/api/latest/docs/openapi.json
- **API base URL:** `https://pipes.turbot.com/api/latest`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://turbot.com/pipes/docs/develop/query-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
