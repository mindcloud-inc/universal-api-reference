# Smartsheet: Native API Reference

A consolidated summary of Smartsheet's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.smartsheet.com/api/smartsheet/openapi
- **OpenAPI specification:** https://developers.smartsheet.com/_bundle/api/smartsheet/openapi.json?download=
- **API base URL:** `https://api.smartsheet.com/2.0`

## Authentication

### OAuth2

Connect Smartsheet with OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.smartsheet.com/b/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.smartsheet.com/2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ADMIN_USERS ADMIN_SHEETS ADMIN_WEBHOOKS ADMIN_WORKSPACES CREATE_SHEETS DELETE_SHEETS READ_CONTACTS READ_EVENTS READ_SHEETS READ_USERS SHARE_SHEETS WRITE_SHEETS READ_ROW_EMAILS WRITE_ROW_EMAILS ADMIN_SIGHTS CREATE_WORKSPACES`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.smartsheet.com/2.0/token.

[Official authentication documentation](https://developers.smartsheet.com/api/smartsheet/guides/advanced-topics/oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numericDates` | query | `boolean` | no | Return date and time values as Unix epoch milliseconds. |

The total page count is read from `totalPages`. The current page number is read from `pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Rows](actions/copy-rows.md) | `POST /sheets/:sheetId/rows/copy` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/copy-rows) |
| [Copy Sheet](actions/copy-sheet.md) | `POST /sheets/:sheetId/copy` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/copy-sheet) |
| [Create Column](actions/create-column.md) | `POST /sheets/:sheetId/columns` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/columns/add-column) |
| [Create Folder in Workspace](actions/create-folder-in-workspace.md) | `POST /workspaces/:workspaceId/folders` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/folders/create-folder-in-workspace) |
| [Create Link Attachment on Sheet](actions/create-link-attachment-on-sheet.md) | `POST /sheets/:sheetId/attachments` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/attachments/attachments-attachtosheet) |
| [Create Row](actions/create-row.md) | `POST /sheets/:sheetId/rows` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/add-rows) |
| [Create Sheet](actions/create-sheet.md) | `POST /sheets` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/create-sheet) |
| [Create Sheet in Folder](actions/create-sheet-in-folder.md) | `POST /folders/:folderId/sheets` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/create-sheet-in-folder) |
| [Create Sheet in Workspace](actions/create-sheet-in-workspace.md) | `POST /workspaces/:workspaceId/sheets` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/create-sheet-in-workspace) |
| [Delete Column](actions/delete-column.md) | `DELETE /sheets/:sheetId/columns/:columnId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/columns/delete-column) |
| [Delete Rows](actions/delete-rows.md) | `DELETE /sheets/:sheetId/rows` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/delete-rows) |
| [Delete Sheet](actions/delete-sheet.md) | `DELETE /sheets/:sheetId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/delete-sheet) |
| [Get Row](actions/get-row.md) | `GET /sheets/:sheetId/rows/:rowId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/get-row) |
| [Get Sheet](actions/get-sheet.md) | `GET /sheets/:sheetId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/getsheet) |
| [Get Sheet Summary](actions/get-sheet-summary.md) | `GET /sheets/:sheetId/summary` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheetsummary/sheetsummary) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/workspaces/get-workspace) |
| [List Columns](actions/list-columns.md) | `GET /sheets/:sheetId/columns` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/columns/columns-listonsheet) |
| [List Folder Children](actions/list-folder-children.md) | `GET /folders/:folderId/children` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/folders/list-folder-children) |
| [List Reports](actions/list-reports.md) | `GET /reports` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/reports/getreports) |
| [List Sheet Attachments](actions/list-sheet-attachments.md) | `GET /sheets/:sheetId/attachments` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/attachments/attachments-listonsheet) |
| [List Sheets](actions/list-sheets.md) | `GET /sheets` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/list-sheets) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/workspaces/list-workspaces) |
| [Move Rows](actions/move-rows.md) | `POST /sheets/:sheetId/rows/move` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/move-rows) |
| [Move Sheet](actions/move-sheet.md) | `POST /sheets/:sheetId/move` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/move-sheet) |
| [Search Smartsheet](actions/search-smartsheet.md) | `GET /search` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/search/list-search) |
| [Sort Sheet Rows](actions/sort-sheet-rows.md) | `POST /sheets/:sheetId/sort` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/sort-rows) |
| [Update Column](actions/update-column.md) | `PUT /sheets/:sheetId/columns/:columnId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/columns/update-column) |
| [Update Row](actions/update-row.md) | `PUT /sheets/:sheetId/rows` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/rows/update-rows) |
| [Update Sheet](actions/update-sheet.md) | `PUT /sheets/:sheetId` | [docs](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/update-sheet) |
