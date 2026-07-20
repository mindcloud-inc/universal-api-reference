# NocoDB: Native API Reference

A consolidated summary of NocoDB's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://nocodb.com/docs/product-docs/developer-resources/rest-apis
- **OpenAPI specification:** https://nocodb.com/apis/v3/swagger-v3.json
- **API base URL:** `https://app.nocodb.com`

## Authentication

### API Token

Connect with a NocoDB API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://nocodb.com/docs/product-docs/account-settings/api-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `pageSize` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `allof`, `anyof`, `btw`, `eq`, `ge`, `gt`, `in`, `is`, `isWithin`, `isnot`, `le`, `like`, `lt`, `nallof`, `nanyof`, `neq`, `nlike`.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Table Records](actions/count-table-records.md) | `GET /api/v3/data/:baseId/:tableId/count` | [docs](https://nocodb.com/apis/v3/data) |
| [Create Base](actions/create-base.md) | `POST /api/v3/meta/workspaces/:workspaceId/bases` | [docs](https://nocodb.com/apis/v3/meta) |
| [Create Field](actions/create-field.md) | `POST /api/v3/meta/bases/:baseId/tables/:tableId/fields` | [docs](https://nocodb.com/apis/v3/meta) |
| [Create Table](actions/create-table.md) | `POST /api/v3/meta/bases/:baseId/tables` | [docs](https://nocodb.com/apis/v3/meta) |
| [Create Table Records](actions/create-table-records.md) | `POST /api/v3/data/:baseId/:tableId/records` | [docs](https://nocodb.com/apis/v3/data) |
| [Delete Base](actions/delete-base.md) | `DELETE /api/v3/meta/bases/:baseId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Delete Field](actions/delete-field.md) | `DELETE /api/v3/meta/bases/:baseId/fields/:fieldId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Delete Table](actions/delete-table.md) | `DELETE /api/v3/meta/bases/:baseId/tables/:tableId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Delete Table Records](actions/delete-table-records.md) | `DELETE /api/v3/data/:baseId/:tableId/records` | [docs](https://nocodb.com/apis/v3/data) |
| [Get Base](actions/get-base.md) | `GET /api/v3/meta/bases/:baseId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Get Field](actions/get-field.md) | `GET /api/v3/meta/bases/:baseId/fields/:fieldId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Get Record](actions/get-record.md) | `GET /api/v3/data/:baseId/:tableId/records/:recordId` | [docs](https://nocodb.com/apis/v3/data) |
| [Get Table](actions/get-table.md) | `GET /api/v3/meta/bases/:baseId/tables/:tableId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Link Records](actions/link-records.md) | `POST /api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId` | [docs](https://nocodb.com/apis/v3/data) |
| [List Bases](actions/list-bases.md) | `GET /api/v3/meta/workspaces/:workspaceId/bases` | [docs](https://nocodb.com/apis/v3/meta) |
| [List Linked Records](actions/list-linked-records.md) | `GET /api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId` | [docs](https://nocodb.com/apis/v3/data) |
| [List Table Records](actions/list-table-records.md) | `GET /api/v3/data/:baseId/:tableId/records` | [docs](https://nocodb.com/apis/v3/data) |
| [List Tables](actions/list-tables.md) | `GET /api/v3/meta/bases/:baseId/tables` | [docs](https://nocodb.com/apis/v3/meta) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/v3/meta/workspaces` | [docs](https://nocodb.com/apis/v3/meta) |
| [Rename Table](actions/rename-table.md) | `PATCH /api/v3/meta/bases/:baseId/tables/:tableId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Unlink Records](actions/unlink-records.md) | `DELETE /api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId` | [docs](https://nocodb.com/apis/v3/data) |
| [Update Base](actions/update-base.md) | `PATCH /api/v3/meta/bases/:baseId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Update Field](actions/update-field.md) | `PATCH /api/v3/meta/bases/:baseId/fields/:fieldId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Update Table Description](actions/update-table-description.md) | `PATCH /api/v3/meta/bases/:baseId/tables/:tableId` | [docs](https://nocodb.com/apis/v3/meta) |
| [Update Table Records](actions/update-table-records.md) | `PATCH /api/v3/data/:baseId/:tableId/records` | [docs](https://nocodb.com/apis/v3/data) |
| [Upload Attachment to Cell](actions/upload-attachment-to-cell.md) | `POST /api/v3/data/:baseId/:modelId/records/:recordId/fields/:fieldId/upload` | [docs](https://nocodb.com/apis/v3/data) |
