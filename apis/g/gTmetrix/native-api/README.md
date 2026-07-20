# GTmetrix: Native API Reference

A consolidated summary of GTmetrix's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://gtmetrix.com/api/docs/2.0/
- **OpenAPI specification:** https://gtmetrix.com/api/gtmetrix-openapi-v2.0.json
- **API base URL:** `https://gtmetrix.com/api/2.0`

## Authentication

### Basic

Use your GTmetrix API key as the username and leave the password blank. GTmetrix authenticates API requests with HTTP Basic auth.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://gtmetrix.com/api/docs/2.0/#api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Status](actions/get-account-status.md) | `GET /status` | [docs](https://gtmetrix.com/api/docs/2.0/#api-status) |
