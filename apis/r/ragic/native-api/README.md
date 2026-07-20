# Ragic: Native API Reference

A consolidated summary of Ragic's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://www.ragic.com/docs/api/en/
- **API base URL:** `{serverUrl}/mindcloud`

## Authentication

### API Key

Authenticate with a Ragic API key over HTTP Basic Auth.

### Credentials

- **API Key:** `apiKey` · required
- **Server URL:** `serverUrl` · required · Exact Ragic server hostname for the workspace, such as https://na5.ragic.com.
- **Account Name:** `accountName` · required · Ragic account or database segment from the workspace URL, such as sims.
- **App Name:** `appName` · required · Ragic application path segment used in the authenticated URL, for example mindcloud.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ragic.com/intl/en/doc-api/24/HTTP-Basic-authentication-with-Ragic-API-Key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string. Supported operators: `eq`, `eqeq`, `gt`, `gte`, `like`, `lt`, `lte`, `regex`.

## Sorting

Set the sort field with `order` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Record Comment](actions/add-record-comment.md) | `POST /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-comment) |
| [Create Record](actions/create-record.md) | `POST /:tabFolderPath/:sheetIndex` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-create) |
| [Delete Record](actions/delete-record.md) | `DELETE /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-delete) |
| [Execute Action Button](actions/execute-action-button.md) | `POST /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-action) |
| [Get Attachment / File](actions/get-attachment-file.md) | `GET {{credentials.serverUrl}}/file.jsp` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-files) |
| [Get Custom Print Report](actions/get-custom-print-report.md) | `GET /:tabFolderPath/:sheetIndex/:recordId.carbone` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-exports/operation/getRecordCarbone) |
| [Get Mass Task Status](actions/get-mass-task-status.md) | `GET /` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Task-Progress-Tracking) |
| [Get Record](actions/get-record.md) | `GET /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-format/operation/getRecord) |
| [Get Record As Excel](actions/get-record-as-excel.md) | `GET /:tabFolderPath/:sheetIndex/:recordId.xlsx` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-exports/operation/getRecordExcel) |
| [Get Record As HTML](actions/get-record-as-html.md) | `GET /:tabFolderPath/:sheetIndex/:recordId.xhtml` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-exports/operation/getRecordHtml) |
| [Get Record As PDF](actions/get-record-as-pdf.md) | `GET /:tabFolderPath/:sheetIndex/:recordId.pdf` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-exports/operation/getRecordPdf) |
| [Get Webhook Public Key As PEM](actions/get-webhook-public-key-as-pem.md) | `GET {{credentials.serverUrl}}/api/http/getWebhookSignaturePublicKey.jsp` | [docs](https://www.ragic.com/docs/api/en/#tag/webhooks-signature/Get-Public-Key) |
| [Get Webhook Public Key As String](actions/get-webhook-public-key-as-string.md) | `GET {{credentials.serverUrl}}/api/http/getWebhookSignaturePublicKey.jsp` | [docs](https://www.ragic.com/docs/api/en/#tag/webhooks-signature/Get-Public-Key) |
| [Import From URL](actions/import-from-url.md) | `POST /:tabFolderPath/:sheetIndex` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-import) |
| [List Action Buttons](actions/list-action-buttons.md) | `GET /:tabFolderPath/:sheetIndex/metadata/actionButton` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-action) |
| [List Records](actions/list-records.md) | `GET /:tabFolderPath/:sheetIndex` | [docs](https://www.ragic.com/docs/api/en/#tag/reading-format/operation/listRecords) |
| [Lock Record](actions/lock-record.md) | `POST /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-lock) |
| [Mass Approve Records](actions/mass-approve-records.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massApproval` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Approval) |
| [Mass Execute Action Button](actions/mass-execute-action-button.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massActionButton` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Action-Button) |
| [Mass Lock Records](actions/mass-lock-records.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massLock` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Lock) |
| [Mass Reject Records](actions/mass-reject-records.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massApproval` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Approval) |
| [Mass Search And Replace](actions/mass-search-and-replace.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massSearchReplace` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Search-And-Replace) |
| [Mass Unlock Records](actions/mass-unlock-records.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massLock` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Lock) |
| [Mass Update Records](actions/mass-update-records.md) | `POST /:tabFolderPath/:sheetIndex/massOperation/massUpdate` | [docs](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Update) |
| [Patch Record](actions/patch-record.md) | `PATCH /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-modify) |
| [Replace Record](actions/replace-record.md) | `PUT /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-modify) |
| [Unlock Record](actions/unlock-record.md) | `POST /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-lock) |
| [Update Record](actions/update-record.md) | `POST /:tabFolderPath/:sheetIndex/:recordId` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-modify) |
| [Upload Files and Images](actions/upload-files-and-images.md) | `POST /:tabFolderPath/:sheetIndex` | [docs](https://www.ragic.com/docs/api/en/#tag/writing-upload) |
