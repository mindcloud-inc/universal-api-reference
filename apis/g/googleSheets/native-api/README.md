# Google Sheets: Native API Reference

A consolidated summary of Google Sheets's API configuration and 15 documented operations.

- **API base URL:** `https://sheets.googleapis.com/v4`

## Authentication

### Google OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/spreadsheets https://www.googleapis.com/auth/drive.file`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON. Response data is read from `sheets`.

## Pagination

Use `pageSize` in the query string to set the page size (default 1000; maximum 1000). Use `pageToken` in the query string as the pagination cursor.

## Retry behavior

Wait 60000 ms before the first retry. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append Rows](actions/append-rows.md) | `POST spreadsheets/:spreadsheetId/values/:worksheet!:range:append` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/append) |
| [Batch Update Spreadsheet Values](actions/batch-update-spreadsheet-values.md) | `POST spreadsheets/:spreadsheetId/:batchUpdate` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchUpdate) |
| [Clear Row](actions/clear-row.md) | `POST spreadsheets/:spreadsheetId/values:method` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchClear) |
| [Create Row](actions/create-row.md) | `POST spreadsheets/:spreadsheetId/values/:worksheet!:range:append` | [docs](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/append) |
| [Create Spreadsheet](actions/create-spreadsheet.md) | `POST spreadsheets` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/create) |
| [Create Worksheet](actions/create-worksheet.md) | `POST spreadsheets/:spreadsheetId:batchUpdate` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/batchUpdate) |
| [Delete Row](actions/delete-row.md) | `POST spreadsheets/:spreadsheetId:method` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/batchUpdate) |
| [Delete Rows](actions/delete-rows.md) | `POST spreadsheets/:spreadsheetId:method` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/batchUpdate) |
| [Get Spreadsheet Metadata](actions/get-spreadsheet-metadata.md) | `GET spreadsheets/:spreadsheetId` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/get) |
| [List Spreadsheet Columns](actions/list-spreadsheet-columns.md) | `GET spreadsheets/:spreadsheetId/values:method` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchGet) |
| [List Spreadsheet Rows](actions/list-spreadsheet-rows.md) | `GET spreadsheets/:spreadsheetId/values:method` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchGet) |
| [List Spreadsheet Worksheets](actions/list-spreadsheet-worksheets.md) | `GET spreadsheets/:spreadsheetId?fields=sheets.properties` | [docs](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/get) |
| [List Spreadsheets](actions/list-spreadsheets.md) | `GET https://www.googleapis.com/drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [Update Cell](actions/update-cell.md) | `PUT spreadsheets/:spreadsheetId/values/:worksheet!:cell` | [docs](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/update) |
| [Update Spreadsheet Row](actions/update-spreadsheet-row.md) | `PUT spreadsheets/:spreadsheetId/values/:worksheet!:row::row` | [docs](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/update) |
