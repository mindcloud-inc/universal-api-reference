# USAC: Native API Reference

A consolidated summary of USAC's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://dev.socrata.com/
- **API base URL:** `https://opendata.usac.org/api/`

## Authentication

### None

This API does not require request authentication.

### Basic

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

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Data](actions/get-data.md) | `GET resource/:resourceId.json` | [docs](https://dev.socrata.com/docs/filtering) |
| [Get Data Count](actions/get-data-count.md) | `GET resource/:resourceId.json` | [docs](https://dev.socrata.com/docs/queries/select) |
| [List Dataset Categories](actions/list-dataset-categories.md) | `GET api/browse_config` | [docs](none) |
| [List Datasets](actions/list-datasets.md) | `GET catalog/v1` | [docs](none) |
