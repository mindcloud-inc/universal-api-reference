# Piped: Native API Reference

A consolidated summary of Piped's API configuration, with links to official documentation.

- **Official docs:** https://docs.piped.video
- **OpenAPI specification:** https://raw.githubusercontent.com/TeamPiped/OpenAPI/main/swagger.yaml
- **API base URL:** `https://api.piped.private.coffee`

## Authentication

### Session Token

Raw Piped session token for authenticated account routes. Public routes do not require authentication.

### Credentials

- **Session Token:** `authorization` · optional · Raw Piped session token returned by the register/login endpoints and sent exactly as the Authorization header value on authenticated routes.

Send these headers with each API request:

```http
Authorization: <authorization>
```

[Official authentication documentation](https://docs.piped.video/docs/api-documentation/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.
