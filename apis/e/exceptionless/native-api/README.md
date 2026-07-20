# Exceptionless: Native API Reference

A consolidated summary of Exceptionless's API configuration, with links to official documentation.

- **Official docs:** https://api.exceptionless.io/docs
- **API base URL:** `https://api.exceptionless.com/api/v2`

## Authentication

### Project or User Token

Connect with an Exceptionless bearer token. Project tokens support project configuration and event submission; user-scoped tokens are required for management reads and writes.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://exceptionless.com/docs/api/getting-events/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
