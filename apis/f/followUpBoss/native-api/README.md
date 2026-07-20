# Follow Up Boss - Legacy: Native API Reference

A consolidated summary of Follow Up Boss - Legacy's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.followupboss.com/reference
- **OpenAPI specification:** https://docs.followupboss.com/reference/getting-started
- **API base URL:** `https://api.followupboss.com/v1/`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **System:** `system` · required · Registered X-System header value required by Follow Up Boss for your integration.
- **System Key:** `systemKey` · required · Registered X-System-Key header value required by Follow Up Boss for your integration.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.followupboss.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string. Supported operators: `between`, `contain`, `empty`, `eq`, `exist`, `gt`, `gte`, `includes`, `lt`, `lte`, `ncontain`, `ne`, `nempty`, `nexist`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Events](actions/list-events.md) | `GET events` | [docs](https://docs.followupboss.com/reference/events-get) |
| [List People](actions/list-people.md) | `GET people` | [docs](https://docs.followupboss.com/reference/people-get) |
