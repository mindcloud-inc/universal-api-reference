# Guru: Native API Reference

A consolidated summary of Guru's API configuration, with links to official documentation.

- **Official docs:** https://developer.getguru.com/reference
- **OpenAPI specification:** https://api.getguru.com/api/v1/openapi.json
- **API base URL:** `https://api.getguru.com/api/v1`

## Authentication

### Basic Token Auth

Use a Guru user token or collection token with Basic authentication.

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

[Official authentication documentation](https://developer.getguru.com/docs/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
