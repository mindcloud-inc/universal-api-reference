# Baserow: Native API Reference

A consolidated summary of Baserow's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://api.baserow.io/api/redoc/
- **OpenAPI specification:** https://api.baserow.io/api/schema.json
- **API base URL:** `https://api.baserow.io`

## Authentication

### Database token

Authenticate Baserow row and table API requests with a workspace-scoped database token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://baserow.io/user-docs/personal-api-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_by` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Create Rows](actions/batch-create-rows.md) | `POST /api/database/rows/table/:table_id/batch/` | [docs](https://api.baserow.io/api/redoc/#operation/batch_create_database_table_rows) |
| [Batch Delete Rows](actions/batch-delete-rows.md) | `POST /api/database/rows/table/:table_id/batch-delete/` | [docs](https://api.baserow.io/api/redoc/#operation/batch_delete_database_table_rows) |
| [Batch Update Rows](actions/batch-update-rows.md) | `PATCH /api/database/rows/table/:table_id/batch/` | [docs](https://api.baserow.io/api/redoc/#operation/batch_update_database_table_rows) |
| [Check Database Token](actions/check-database-token.md) | `GET /api/database/tokens/check/` | [docs](https://api.baserow.io/api/redoc/#operation/check_database_token) |
| [Create Field](actions/create-field.md) | `POST /api/database/fields/table/:table_id/` | [docs](https://api.baserow.io/api/redoc/#operation/create_database_table_field) |
| [Create Row](actions/create-row.md) | `POST /api/database/rows/table/:table_id/` | [docs](https://api.baserow.io/api/redoc/#operation/create_database_table_row) |
| [Delete Row](actions/delete-row.md) | `DELETE /api/database/rows/table/:table_id/:row_id/` | [docs](https://api.baserow.io/api/redoc/#operation/delete_database_table_row) |
| [Get Row](actions/get-row.md) | `GET /api/database/rows/table/:table_id/:row_id/` | [docs](https://api.baserow.io/api/redoc/#operation/get_database_table_row) |
| [List All Tables](actions/list-all-tables.md) | `GET /api/database/tables/all-tables/` | [docs](https://api.baserow.io/api/redoc/#operation/list_all_token_tables) |
| [List Fields](actions/list-fields.md) | `GET /api/database/fields/table/:table_id/` | [docs](https://api.baserow.io/api/redoc/#operation/list_database_table_fields) |
| [List Row Names](actions/list-row-names.md) | `GET /api/database/rows/names/` | [docs](https://api.baserow.io/api/redoc/#operation/list_database_table_row_names) |
| [List Rows](actions/list-rows.md) | `GET /api/database/rows/table/:table_id/` | [docs](https://api.baserow.io/api/redoc/#operation/list_database_table_rows) |
| [Move Row](actions/move-row.md) | `PATCH /api/database/rows/table/:table_id/:row_id/move/` | [docs](https://api.baserow.io/api/redoc/#operation/move_database_table_row) |
| [Password Field Authentication](actions/password-field-authentication.md) | `POST /api/database/fields/password-authentication/` | [docs](https://api.baserow.io/api/redoc/#operation/password_field_authentication) |
| [Update Row](actions/update-row.md) | `PATCH /api/database/rows/table/:table_id/:row_id/` | [docs](https://api.baserow.io/api/redoc/#operation/update_database_table_row) |
| [Upload File](actions/upload-file.md) | `POST /api/user-files/upload-file/` | [docs](https://api.baserow.io/api/redoc/#operation/upload_file) |
| [Upload File Via URL](actions/upload-file-via-url.md) | `POST /api/user-files/upload-via-url/` | [docs](https://api.baserow.io/api/redoc/#operation/upload_via_url) |
