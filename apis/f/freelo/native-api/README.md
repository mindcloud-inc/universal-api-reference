# Freelo: Native API Reference

A consolidated summary of Freelo's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://api.freelo.io/docs/v1/freelo-api
- **OpenAPI specification:** https://api.freelo.io/docs/v1/freelo-api.yaml
- **API base URL:** `https://api.freelo.io/v1`

## Authentication

### Basic Authentication

Use your Freelo account email as username and your API key as password.

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

[Official authentication documentation](https://www.freelo.io/en/help/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud/1.0` |

Responses from this API use JSON.

## Pagination

Use `p` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://api.freelo.io/docs/v1/freelo-api) |
| [List All Projects](actions/list-all-projects.md) | `GET /all-projects` | [docs](https://api.freelo.io/docs/v1/freelo-api) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.freelo.io/docs/v1/freelo-api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.freelo.io/docs/v1/freelo-api) |
