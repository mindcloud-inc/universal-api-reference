# easyDNS: Native API Reference

A consolidated summary of easyDNS's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.sandbox.rest.easydns.net:3001/
- **OpenAPI specification:** https://docs.sandbox.rest.easydns.net:3001/swagger3.yaml
- **API base URL:** `https://sandbox.rest.easydns.net`

## Authentication

### Basic

Authenticate with your easyDNS API token as the username and your easyDNS API key as the password.

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

[Official authentication documentation](https://docs.sandbox.rest.easydns.net/loadpage.php?pid=5)

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
| [Get User Info](actions/get-user-info.md) | `GET /user` | [docs](https://docs.sandbox.rest.easydns.net/loadpage.php?pid=18) |
