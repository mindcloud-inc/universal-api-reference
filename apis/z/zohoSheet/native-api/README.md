# Zoho Sheet: Native API Reference

A consolidated summary of Zoho Sheet's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/sheet/help/api/v2/
- **API base URL:** `https://sheet.zoho.com/api/v2/`

## Authentication

### OAuth 2.0

Connect Zoho Sheet with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoSheet.dataAPI.READ,ZohoSheet.dataAPI.UPDATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/sheet/help/api/v2/#serverapp)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Records to Table](actions/add-records-to-table.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Add-records-to-table) |
| [Add Records to Worksheet](actions/add-records-to-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Add-records-to-worksheet) |
| [Copy Workbook](actions/copy-workbook.md) | `POST /copy` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-Copy-workbook) |
| [Create Table](actions/create-table.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Create-table) |
| [Create Workbook](actions/create-workbook.md) | `POST /create` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-Create-workbook) |
| [Create Worksheet](actions/create-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKSHEET-Create-worksheet) |
| [Delete Records from Table](actions/delete-records-from-table.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Delete-records-from-table) |
| [Delete Records from Worksheet](actions/delete-records-from-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Delete-records-from-worksheet) |
| [Delete Worksheet](actions/delete-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKSHEET-Delete-worksheet) |
| [Fetch Records from Table](actions/fetch-records-from-table.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Fetch-records-from-table) |
| [Fetch Records from Worksheet](actions/fetch-records-from-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Fetch-records-from-worksheet) |
| [Find](actions/find.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Find) |
| [Find and Replace](actions/find-and-replace.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Find-and-replace) |
| [Get Content of Range](actions/get-content-of-range.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Get-content-of-range) |
| [Get Used Area](actions/get-used-area.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Get-used-area) |
| [List All Tables](actions/list-all-tables.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-List-all-tables) |
| [List All Templates](actions/list-all-templates.md) | `POST /templates` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-List-all-templates) |
| [List All Workbooks](actions/list-all-workbooks.md) | `POST /workbooks` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-List-all-workbooks) |
| [List All Worksheets](actions/list-all-worksheets.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKSHEET-List-all-worksheets) |
| [Rename Worksheet](actions/rename-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#WORKSHEET-Rename-worksheet) |
| [Set Content to Range](actions/set-content-to-range.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Set-content-to-range) |
| [Update Records in Table](actions/update-records-in-table.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Update-records-in-table) |
| [Update Records in Worksheet](actions/update-records-in-worksheet.md) | `POST /:resourceId` | [docs](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Update-records-in-worksheet) |
