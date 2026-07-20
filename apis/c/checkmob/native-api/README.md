# Checkmob: Native API Reference

A consolidated summary of Checkmob's API configuration, with links to official documentation.

- **Official docs:** https://api-integration.checkmob.com/index.html
- **OpenAPI specification:** https://api-integration.checkmob.com/swagger/v1/swagger.json
- **API base URL:** `https://api-integration.checkmob.com`

## Authentication

### Checkmob Login

Authenticate with a Checkmob login and password, then exchange them for a short-lived bearer token.

### Credentials

- **Password:** `password` · required · Your Checkmob password.
- **Login:** `login` · required · Your Checkmob login email or username.

Send these headers with each API request:

```http
Authorization: Bearer <custom.data.token.accessToken>
```

[Official authentication documentation](https://api-integration.checkmob.com/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Accept-Language` | `en-US` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `numberOfRows` in the request body to set the page size (default 100). Use `numberOfRowsSkipped` in the request body as the record offset; numbering starts at 0.
