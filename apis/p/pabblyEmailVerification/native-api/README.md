# Pabbly Email Verification: Native API Reference

A consolidated summary of Pabbly Email Verification's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.pabbly.com/
- **API base URL:** `https://verify.pabbly.com/api/v1`

## Authentication

### Basic Auth

Pabbly Email Verification uses Basic Auth with API Key as username and Secret Key as password.

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

[Official authentication documentation](https://apidocs.pabbly.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Verify Single Email](actions/verify-single-email.md) | `POST /email-lists/verify-single` | [docs](https://apidocs.pabbly.com/) |
