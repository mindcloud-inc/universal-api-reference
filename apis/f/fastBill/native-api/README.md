# FastBill: Native API Reference

A consolidated summary of FastBill's API configuration, with links to official documentation.

- **Official docs:** https://apidocs.fastbill.com/fastbill/en/fundamentals.html
- **API base URL:** `https://my.fastbill.com/api/1.0`

## Authentication

### Basic

Use the main FastBill user email address as the username and the FastBill API key as the password.

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

[Official authentication documentation](https://apidocs.fastbill.com/fastbill/en/fundamentals.html#authentification)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `LIMIT` in the request body to set the page size (default 10; maximum 100). Use `OFFSET` in the request body as the record offset.
