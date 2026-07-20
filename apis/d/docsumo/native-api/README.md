# Docsumo: Native API Reference

A consolidated summary of Docsumo's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://support.docsumo.com/reference
- **API base URL:** `https://app.docsumo.com`

## Authentication

### API Key

Authenticate Docsumo using an API key from your Docsumo account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://support.docsumo.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Files In Folder](actions/add-files-in-folder.md) | `POST /api/v1/eevee/documents/upload/` | [docs](https://support.docsumo.com/reference/post_api-v1-eevee-documents-upload) |
| [Add Table](actions/add-table.md) | `POST /api/v1/raichu/drop_down/db/add/` | [docs](https://support.docsumo.com/reference/post_api-v1-raichu-drop-down-db-add) |
| [Add Table Row](actions/add-table-row.md) | `POST /api/v1/raichu/drop_down/db/addrow/:ddid/` | [docs](https://support.docsumo.com/reference/add-new-line) |
| [Create Folder](actions/create-folder.md) | `POST /api/v1/mew/folder/add/` | [docs](https://support.docsumo.com/reference/folder-creation) |
| [Delete Cases](actions/delete-cases.md) | `POST /api/v1/external/agents/:casetype_id/cases/bulk/delete` | [docs](https://support.docsumo.com/reference/bulk-delete-cases) |
| [Delete Document](actions/delete-document.md) | `DELETE /api/v1/eevee/apikey/delete/:doc_id/` | [docs](https://support.docsumo.com/reference/api-v1-user-document-delete) |
| [Delete Table](actions/delete-table.md) | `DELETE /api/v1/raichu/drop_down/db/delete/` | [docs](https://support.docsumo.com/reference/delete-table) |
| [Get Bank Statement Analytics](actions/get-bank-statement-analytics.md) | `GET /api/v1/mew/usbs-analytics/:doc_id/` | [docs](https://support.docsumo.com/reference/api-v1-bank-statement-analytics-api) |
| [Get Case Overview](actions/get-case-overview.md) | `GET /api/v1/external/agents/:casetype_id/case/:case_id` | [docs](https://support.docsumo.com/reference/get-case-overview) |
| [Get Case Type Details](actions/get-case-type-details.md) | `GET /api/v1/external/agents/:casetype_id` | [docs](https://support.docsumo.com/reference/get-casetype-details) |
| [Get Document Details](actions/get-document-details.md) | `GET /api/v1/eevee/apikey/documents/detail/:doc_id/` | [docs](https://support.docsumo.com/reference/api-v1-user-documents-detail) |
| [Get Document Review URL](actions/get-document-review-url.md) | `GET /api/v1/eevee/apikey/review-url/:doc_id/` | [docs](https://support.docsumo.com/reference/api-v1-user-documents-review-url) |
| [Get Documents Summary](actions/get-documents-summary.md) | `GET /api/v1/mew/apikey/documents/summary/` | [docs](https://support.docsumo.com/reference/api-v1-user-documents-summary) |
| [Get Extracted Data](actions/get-extracted-data.md) | `GET /api/v1/eevee/apikey/data/simplified/:doc_id/` | [docs](https://support.docsumo.com/reference/api-v1-extracted-data-simplified) |
| [Get Folder Review URL](actions/get-folder-review-url.md) | `GET /api/v1/eevee/apikey/review-url-folder/:folder_id/` | [docs](https://support.docsumo.com/reference/get_api-v1-eevee-apikey-review-url-folder-folder-id) |
| [Get Split File URLs](actions/get-split-file-urls.md) | `GET /api/v1/mew/apikey/autosplit/files/:original_doc_id/` | [docs](https://support.docsumo.com/reference/get-split-file) |
| [Get Split Info](actions/get-split-info.md) | `GET /api/v1/mew/apikey/autosplit/info/:original_doc_id/` | [docs](https://support.docsumo.com/reference/get-split-info) |
| [Get Table Data](actions/get-table-data.md) | `GET /api/v1/raichu/drop_down/db/get/:ddid/` | [docs](https://support.docsumo.com/reference/get-table-data) |
| [Get User And Document Types](actions/get-user-and-document-types.md) | `GET /api/v1/eevee/apikey/limit/` | [docs](https://support.docsumo.com/reference/api-v1-user-document-type-list) |
| [List Agents](actions/list-agents.md) | `GET /api/v1/external/agents` | [docs](https://support.docsumo.com/reference/get-all-agents) |
| [List Cases](actions/list-cases.md) | `GET /api/v1/external/agents/:casetype_id/cases` | [docs](https://support.docsumo.com/reference/get-cases-list) |
| [List Documents](actions/list-documents.md) | `GET /api/v1/eevee/apikey/documents/all/` | [docs](https://support.docsumo.com/reference/api-v1-user-documents-list) |
| [List Enabled Document Types](actions/list-enabled-document-types.md) | `GET /api/v1/mew/documents/types/` | [docs](https://support.docsumo.com/reference/user-enabled-doc_types) |
| [Move Documents Between Folders](actions/move-documents-between-folders.md) | `POST /api/v2/eevee/apikey/move/` | [docs](https://support.docsumo.com/reference/move-documents-between-folders) |
| [Run Case Workflow](actions/run-case-workflow.md) | `GET /api/v1/external/agents/:casetype_id/case/:case_id/run` | [docs](https://support.docsumo.com/reference/run-case-workflow) |
| [Run MCA Analysis](actions/run-mca-analysis.md) | `POST /api/v1/skitty/analytics/account-summary/` | [docs](https://support.docsumo.com/reference/mca-analysis) |
| [Set Document Review Status](actions/set-document-review-status.md) | `POST /api/v1/pik/review/:doc_id/:actions/` | [docs](https://support.docsumo.com/reference/api-v1-user-document-review-status) |
| [Update Case](actions/update-case.md) | `PATCH /api/v1/external/agents/:casetype_id/case/:case_id` | [docs](https://support.docsumo.com/reference/update-case) |
| [Update Extracted Field](actions/update-extracted-field.md) | `PATCH /api/v1/pik/apikey/:doc_id/field/:field_id/` | [docs](https://support.docsumo.com/reference/update-a-fields-value) |
| [Update Table Cell](actions/update-table-cell.md) | `PATCH /api/v1/raichu/drop_down/db/update/single/:ddid/` | [docs](https://support.docsumo.com/reference/update-cell) |
| [Upload Case](actions/upload-case.md) | `POST /api/v1/upload-service/agents/casetype/case` | [docs](https://support.docsumo.com/reference/upload-case) |
| [Upload File](actions/upload-file.md) | `POST /api/v1/eevee/apikey/upload/` | [docs](https://support.docsumo.com/reference/api-v1-upload) |
| [Upload File From URL Or Base64](actions/upload-file-from-url-or-base64.md) | `POST /api/v1/eevee/apikey/upload/custom/` | [docs](https://support.docsumo.com/reference/api-v1-upload-custom) |
