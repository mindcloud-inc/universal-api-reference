# Apptoto: Native API Reference

A consolidated summary of Apptoto's API configuration, with links to official documentation.

- **Official docs:** https://apidocs.apptoto.com/reference/introduction
- **API base URL:** `https://api.apptoto.com`

## Authentication

### Basic Authentication

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

[Official authentication documentation](https://apidocs.apptoto.com/reference/basic-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.
