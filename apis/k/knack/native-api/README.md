# Knack: Native API Reference

A consolidated summary of Knack's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.knack.com/v3/reference
- **API base URL:** `https://api.knack.com/v1`

## Authentication

### Custom

Authenticate with explicit Knack Application ID and REST API key headers.

### Credentials

- **Application ID:** `applicationId` · required · Knack application ID from Builder Settings > API.
- **REST API Key:** `apiKey` · required · Knack REST API key from Builder Settings > API.

Send these headers with each API request:

```http
X-Knack-REST-API-Key: <apiKey>
X-Knack-Application-Id: <applicationId>
```

[Official authentication documentation](https://docs.knack.com/docs/object-based-requests)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `records`. The total page count is read from `total_pages`. The current page number is read from `current_page`.

## Pagination

Use `rows_per_page` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_field` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | `POST /objects/:object_key/records` | [docs](https://docs.knack.com/reference/object-based-post) |
| [Create Remote User Login](actions/create-remote-user-login.md) | `POST /applications/{{credentials.applicationId}}/session` | [docs](https://docs.knack.com/reference/remote-user-logins) |
| [Create User Account Record](actions/create-user-account-record.md) | `POST /objects/:object_key/records` | [docs](https://docs.knack.com/v3/docs/managing-user-records) |
| [Delete Record](actions/delete-record.md) | `DELETE /objects/:object_key/records/:record_id` | [docs](https://docs.knack.com/reference/object-based-delete) |
| [Get Record By ID](actions/get-record-by-id.md) | `GET /objects/:object_key/records/:record_id` | [docs](https://docs.knack.com/reference/retrieving-one-record) |
| [List Records](actions/list-records.md) | `GET /objects/:object_key/records` | [docs](https://docs.knack.com/v3/reference/retrieving-records) |
| [Update Record](actions/update-record.md) | `PUT /objects/:object_key/records/:record_id` | [docs](https://docs.knack.com/reference/object-based-put) |
| [Update User Account Record](actions/update-user-account-record.md) | `PUT /objects/:object_key/records/:record_id` | [docs](https://docs.knack.com/v3/docs/managing-user-records) |
| [Update User Roles On Account](actions/update-user-roles-on-account.md) | `PUT /objects/:object_key/records/:record_id` | [docs](https://docs.knack.com/v3/docs/managing-user-records) |
| [Upload File Image Asset](actions/upload-file-image-asset.md) | `POST /applications/{{credentials.applicationId}}/assets/:asset_type/upload` | [docs](https://docs.knack.com/reference/fileimage-uploads) |
