# Short Menu: Native API Reference

A consolidated summary of Short Menu's API configuration, with links to official documentation.

- **Official docs:** https://docs.shortmenu.com/api-reference/introduction
- **OpenAPI specification:** https://shm.to/openapi
- **API base URL:** `https://api.shortmenu.com`

## Authentication

### API Key

Connect with a Short Menu API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.shortmenu.com/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
