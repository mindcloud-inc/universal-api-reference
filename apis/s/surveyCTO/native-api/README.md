# SurveyCTO: Native API Reference

A consolidated summary of SurveyCTO's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developer.surveycto.com/
- **OpenAPI specification:** https://developer.surveycto.com/specs/server-api-v2-spec.json
- **API base URL:** `https://mindcloudsurvey.surveycto.com/api`

## Authentication

### Basic Auth

Authenticate with a SurveyCTO username and password.

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

[Official authentication documentation](https://docs.surveycto.com/05-exporting-and-publishing-data/05-api-access/01.api-access.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–1000). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `orderByDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://developer.surveycto.com/api-v2.html#getDatasets) |
