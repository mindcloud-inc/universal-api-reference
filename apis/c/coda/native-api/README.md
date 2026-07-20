# Coda: Native API Reference

A consolidated summary of Coda's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://coda.io/developers/apis/v1
- **OpenAPI specification:** https://coda.io/apis/v1/openapi.yaml
- **API base URL:** `https://coda.io/apis/v1`

## Authentication

### API Key

Authenticate with a Coda API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://coda.io/developers/apis/v1#section/Using-the-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `limit` in the query string to set the page size (default 25; minimum 1). Use `pageToken` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sortBy` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Doc](actions/create-doc.md) | `POST /docs` | [docs](https://coda.io/developers/apis/v1#tag/Docs/operation/createDoc) |
| [Create Page](actions/create-page.md) | `POST /docs/:docId/pages` | [docs](https://coda.io/developers/apis/v1#tag/Pages/operation/createPage) |
| [Delete Doc](actions/delete-doc.md) | `DELETE /docs/:docId` | [docs](https://coda.io/developers/apis/v1#tag/Docs/operation/deleteDoc) |
| [Delete Page](actions/delete-page.md) | `DELETE /docs/:docId/pages/:pageIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Pages/operation/deletePage) |
| [Delete Row](actions/delete-row.md) | `DELETE /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Rows/operation/deleteRow) |
| [Get Column](actions/get-column.md) | `GET /docs/:docId/tables/:tableIdOrName/columns/:columnIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Columns/operation/getColumn) |
| [Get Control](actions/get-control.md) | `GET /docs/:docId/controls/:controlIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Controls/operation/getControl) |
| [Get Doc](actions/get-doc.md) | `GET /docs/:docId` | [docs](https://coda.io/developers/apis/v1#tag/Docs/operation/getDoc) |
| [Get Formula](actions/get-formula.md) | `GET /docs/:docId/formulas/:formulaIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Formulas/operation/getFormula) |
| [Get Page](actions/get-page.md) | `GET /docs/:docId/pages/:pageIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Pages/operation/getPage) |
| [Get Row](actions/get-row.md) | `GET /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Rows/operation/getRow) |
| [Get Table](actions/get-table.md) | `GET /docs/:docId/tables/:tableIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Tables/operation/getTable) |
| [List Columns](actions/list-columns.md) | `GET /docs/:docId/tables/:tableIdOrName/columns` | [docs](https://coda.io/developers/apis/v1#tag/Columns/operation/listColumns) |
| [List Controls](actions/list-controls.md) | `GET /docs/:docId/controls` | [docs](https://coda.io/developers/apis/v1#tag/Controls/operation/listControls) |
| [List Docs](actions/list-docs.md) | `GET /docs` | [docs](https://coda.io/developers/apis/v1#tag/Docs/operation/listDocs) |
| [List Formulas](actions/list-formulas.md) | `GET /docs/:docId/formulas` | [docs](https://coda.io/developers/apis/v1#tag/Formulas/operation/listFormulas) |
| [List Pages](actions/list-pages.md) | `GET /docs/:docId/pages` | [docs](https://coda.io/developers/apis/v1#tag/Pages/operation/listPages) |
| [List Rows](actions/list-rows.md) | `GET /docs/:docId/tables/:tableIdOrName/rows` | [docs](https://coda.io/developers/apis/v1#tag/Rows/operation/listRows) |
| [List Tables](actions/list-tables.md) | `GET /docs/:docId/tables` | [docs](https://coda.io/developers/apis/v1#tag/Tables/operation/listTables) |
| [Push Button](actions/push-button.md) | `POST /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName/buttons/:columnIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Rows/operation/pushButton) |
| [Update Doc](actions/update-doc.md) | `PATCH /docs/:docId` | [docs](https://coda.io/developers/apis/v1#tag/Docs/operation/updateDoc) |
| [Update Page](actions/update-page.md) | `PUT /docs/:docId/pages/:pageIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Pages/operation/updatePage) |
| [Update Row](actions/update-row.md) | `PUT /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName` | [docs](https://coda.io/developers/apis/v1#tag/Rows/operation/updateRow) |
| [Upsert Rows](actions/upsert-rows.md) | `POST /docs/:docId/tables/:tableIdOrName/rows` | [docs](https://coda.io/developers/apis/v1#tag/Rows/operation/upsertRows) |
