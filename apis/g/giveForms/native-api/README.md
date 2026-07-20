# GiveForms: Native API Reference

A consolidated summary of GiveForms's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.giveforms.com/support-article/rest-api
- **API base URL:** `https://app.giveforms.com/api/v1`

## Authentication

### Basic Auth

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

[Official authentication documentation](https://www.giveforms.com/support-article/rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Donations](actions/list-donations.md) | `GET /donations` | [docs](https://www.giveforms.com/support-article/rest-api) |
