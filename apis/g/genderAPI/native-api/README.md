# Gender API: Native API Reference

A consolidated summary of Gender API's API configuration, with links to official documentation.

- **Official docs:** https://gender-api.com/en/api-docs/v2
- **OpenAPI specification:** https://gender-api.com/openapi/openapi.yml
- **API base URL:** `https://gender-api.com`

## Authentication

### API Token

Use a Gender API bearer token for all v2 endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://gender-api.com/en/account/auth-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
