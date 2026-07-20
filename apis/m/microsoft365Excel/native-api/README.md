# Microsoft 365 Excel: Native API Reference

A consolidated summary of Microsoft 365 Excel's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/excel?view=graph-rest-1.0
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### Microsoft Entra OAuth2

Connect to Microsoft 365 Excel through Microsoft Graph using a Microsoft Entra OAuth 2.0 app registration.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `User.Read Files.ReadWrite offline_access openid profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–999). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Chart](actions/add-chart.md) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts/add` | [docs](https://learn.microsoft.com/en-us/graph/api/chartcollection-add?view=graph-rest-1.0) |
| [Add Table Rows](actions/add-table-rows.md) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/tables('{{tableName}}')/rows/add` | [docs](https://learn.microsoft.com/en-us/graph/api/table-post-rows?view=graph-rest-1.0) |
| [Calculate Workbook](actions/calculate-workbook.md) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/application/calculate` | [docs](https://learn.microsoft.com/en-us/graph/api/workbookapplication-calculate?view=graph-rest-1.0) |
| [Clear Range](actions/clear-range.md) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')/clear` | [docs](https://learn.microsoft.com/en-us/graph/api/range-clear?view=graph-rest-1.0) |
| [Create Table](actions/create-table.md) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/tables/add` | [docs](https://learn.microsoft.com/en-us/graph/api/tablecollection-add?view=graph-rest-1.0) |
| [Create Workbook Session](actions/create-workbook-session.md) | `POST /v1.0/drives/:driveId/items/:driveItemId/workbook/createSession` | [docs](https://learn.microsoft.com/en-us/graph/api/workbook-createsession?view=graph-rest-1.0) |
| [Create Worksheet in Workbook](actions/create-worksheet-in-workbook.md) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets/add` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheetcollection-add?view=graph-rest-1.0) |
| [Delete Worksheet](actions/delete-worksheet.md) | `DELETE /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-delete?view=graph-rest-1.0) |
| [Get Chart Image](actions/get-chart-image.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts('{{chartName}}')/image(width={{width}},height={{height}},fittingMode='{{fittingMode}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/chart-image?view=graph-rest-1.0) |
| [Get My Profile](actions/get-my-profile.md) | `GET /v1.0/me` | [docs](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0) |
| [Get Range](actions/get-range.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/range-get?view=graph-rest-1.0) |
| [Get Used Range](actions/get-used-range.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/usedRange` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-usedrange?view=graph-rest-1.0) |
| [Get Workbook Application](actions/get-workbook-application.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/application` | [docs](https://learn.microsoft.com/en-us/graph/api/workbookapplication-get?view=graph-rest-1.0) |
| [Get Worksheet](actions/get-worksheet.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-get?view=graph-rest-1.0) |
| [List Charts](actions/list-charts.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-list-charts?view=graph-rest-1.0) |
| [List Table Rows](actions/list-table-rows.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/tables('{{tableName}}')/rows` | [docs](https://learn.microsoft.com/en-us/graph/api/table-list-rows?view=graph-rest-1.0) |
| [List Tables](actions/list-tables.md) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/tables` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-list-tables?view=graph-rest-1.0) |
| [List Workbook Tables](actions/list-workbook-tables.md) | `GET /v1.0/sites/:siteId/drive/items/:driveItemId/workbook/tables` | [docs](https://learn.microsoft.com/en-us/graph/api/workbook-list-tables?view=graph-rest-1.0) |
| [List Worksheets](actions/list-worksheets.md) | `GET /v1.0/me/drive/items/:driveItemId/workbook/worksheets` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-list?view=graph-rest-1.0) |
| [Replace Workbook Contents](actions/replace-workbook-contents.md) | `PUT /v1.0/drives/:driveId/items/:driveItemId/content` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0) |
| [Update Range Values](actions/update-range-values.md) | `PATCH /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/range-update?view=graph-rest-1.0) |
| [Update Worksheet](actions/update-worksheet.md) | `PATCH /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-update?view=graph-rest-1.0) |
| [Upload Workbook](actions/upload-workbook.md) | `PUT /v1.0/drives/:driveId/items/:parentFolderId:/:fileName:/content` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0) |
