# Flatfile: Native API Reference

A consolidated summary of Flatfile's API configuration and 51 documented operations, with links to official documentation.

- **Official docs:** https://reference.flatfile.com/overview/welcome
- **OpenAPI specification:** https://reference.flatfile.com/openapi.json
- **API base URL:** `https://api.x.flatfile.com/v1`

## Authentication

### API Key

Flatfile API key authentication using Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://reference.flatfile.com/overview/auth)

## Endpoints (51 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Job](actions/acknowledge-job.md) | `POST /jobs/:jobId/ack` | [docs](https://reference.flatfile.com/api-reference/jobs/ack) |
| [Archive Space](actions/archive-space.md) | `POST /spaces/:spaceId/archive` | [docs](https://reference.flatfile.com/api-reference/spaces/archive-space) |
| [Bulk Update Records](actions/bulk-update-records.md) | `PATCH /sheets/:sheetId/records/bulk-update` | [docs](https://reference.flatfile.com/api-reference/records/bulk-update) |
| [Clone File](actions/clone-file.md) | `POST /files/:fileId/clone` | [docs](https://reference.flatfile.com/api-reference/files/clone) |
| [Complete Job](actions/complete-job.md) | `POST /jobs/:jobId/complete` | [docs](https://reference.flatfile.com/api-reference/jobs/complete) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://reference.flatfile.com/api-reference/jobs/create) |
| [Create Space](actions/create-space.md) | `POST /spaces` | [docs](https://reference.flatfile.com/api-reference/spaces/create) |
| [Create Workbook](actions/create-workbook.md) | `POST /workbooks` | [docs](https://reference.flatfile.com/api-reference/workbooks/create) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:fileId` | [docs](https://reference.flatfile.com/api-reference/files/delete) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/:jobId` | [docs](https://reference.flatfile.com/api-reference/jobs/delete) |
| [Delete Records](actions/delete-records.md) | `DELETE /sheets/:sheetId/records` | [docs](https://reference.flatfile.com/api-reference/records/delete) |
| [Delete Sheet](actions/delete-sheet.md) | `DELETE /sheets/:sheetId` | [docs](https://reference.flatfile.com/api-reference/sheets/delete) |
| [Delete Space](actions/delete-space.md) | `DELETE /spaces/:spaceId` | [docs](https://reference.flatfile.com/api-reference/spaces/delete) |
| [Delete Workbook](actions/delete-workbook.md) | `DELETE /workbooks/:workbookId` | [docs](https://reference.flatfile.com/api-reference/workbooks/delete) |
| [Detect File Header](actions/detect-file-header.md) | `POST /files/detect-header` | [docs](https://reference.flatfile.com/api-reference/files/detect-header) |
| [Download File](actions/download-file.md) | `GET /files/:fileId/download` | [docs](https://reference.flatfile.com/api-reference/files/download) |
| [Duplicate Sheet](actions/duplicate-sheet.md) | `POST /sheets/:sheetId/duplicate` | [docs](https://reference.flatfile.com/api-reference/sheets/duplicate-sheet) |
| [Execute Job](actions/execute-job.md) | `POST /jobs/:jobId/execute` | [docs](https://reference.flatfile.com/api-reference/jobs/execute) |
| [Find And Replace Records](actions/find-and-replace-records.md) | `PUT /sheets/:sheetId/find-replace` | [docs](https://reference.flatfile.com/api-reference/records/find-and-replace) |
| [Get Cell Values](actions/get-cell-values.md) | `GET /sheets/:sheetId/cells` | [docs](https://reference.flatfile.com/api-reference/sheets/get-cell-values) |
| [Get Current Account](actions/get-current-account.md) | `GET /accounts/current` | [docs](https://reference.flatfile.com/api-reference/accounts/get-current) |
| [Get Environment](actions/get-environment.md) | `GET /environments/:environmentId` | [docs](https://reference.flatfile.com/api-reference/environments/get) |
| [Get File](actions/get-file.md) | `GET /files/:fileId` | [docs](https://reference.flatfile.com/api-reference/files/get) |
| [Get Job](actions/get-job.md) | `GET /jobs/:jobId` | [docs](https://reference.flatfile.com/api-reference/jobs/get) |
| [Get Job Execution Plan](actions/get-job-execution-plan.md) | `GET /jobs/:jobId/plan` | [docs](https://reference.flatfile.com/api-reference/jobs/get-execution-plan) |
| [Get Publishable Key](actions/get-publishable-key.md) | `GET /auth/publishable-key` | [docs](https://reference.flatfile.com/api-reference/auth/get-publishable-key) |
| [Get Record Counts](actions/get-record-counts.md) | `GET /sheets/:sheetId/counts` | [docs](https://reference.flatfile.com/api-reference/sheets/get-record-counts) |
| [Get Record Indices](actions/get-record-indices.md) | `GET /sheets/:sheetId/records/indices` | [docs](https://reference.flatfile.com/api-reference/records/indices) |
| [Get Records](actions/get-records.md) | `GET /sheets/:sheetId/records` | [docs](https://reference.flatfile.com/api-reference/records/get) |
| [Get Sheet](actions/get-sheet.md) | `GET /sheets/:sheetId` | [docs](https://reference.flatfile.com/api-reference/sheets/get) |
| [Get Sheet Commits](actions/get-sheet-commits.md) | `GET /sheets/:sheetId/commits` | [docs](https://reference.flatfile.com/api-reference/sheets/get-sheet-commits) |
| [Get Space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://reference.flatfile.com/api-reference/spaces/get) |
| [Get Workbook](actions/get-workbook.md) | `GET /workbooks/:workbookId` | [docs](https://reference.flatfile.com/api-reference/workbooks/get) |
| [Get Workbook Commits](actions/get-workbook-commits.md) | `GET /workbooks/:workbookId/commits` | [docs](https://reference.flatfile.com/api-reference/workbooks/get-workbook-commits) |
| [Insert Records](actions/insert-records.md) | `POST /sheets/:sheetId/records` | [docs](https://reference.flatfile.com/api-reference/records/insert) |
| [List Calculations](actions/list-calculations.md) | `GET /sheets/:sheetId/calculations` | [docs](https://reference.flatfile.com/api-reference/sheets/get-calculations) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://reference.flatfile.com/api-reference/environments/list) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://reference.flatfile.com/api-reference/files/list) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://reference.flatfile.com/api-reference/jobs/list) |
| [List Sheets](actions/list-sheets.md) | `GET /sheets` | [docs](https://reference.flatfile.com/api-reference/sheets/list) |
| [List Spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://reference.flatfile.com/api-reference/spaces/list) |
| [List Workbooks](actions/list-workbooks.md) | `GET /workbooks` | [docs](https://reference.flatfile.com/api-reference/workbooks/list) |
| [Unarchive Space](actions/unarchive-space.md) | `POST /spaces/:spaceId/unarchive` | [docs](https://reference.flatfile.com/api-reference/spaces/unarchive-space) |
| [Update File](actions/update-file.md) | `PATCH /files/:fileId` | [docs](https://reference.flatfile.com/api-reference/files/update) |
| [Update Job](actions/update-job.md) | `PATCH /jobs/:jobId` | [docs](https://reference.flatfile.com/api-reference/jobs/update) |
| [Update Records](actions/update-records.md) | `PUT /sheets/:sheetId/records` | [docs](https://reference.flatfile.com/api-reference/records/update) |
| [Update Sheet](actions/update-sheet.md) | `PATCH /sheets/:sheetId` | [docs](https://reference.flatfile.com/api-reference/sheets/update-sheet) |
| [Update Space](actions/update-space.md) | `PATCH /spaces/:spaceId` | [docs](https://reference.flatfile.com/api-reference/spaces/update) |
| [Update Workbook](actions/update-workbook.md) | `PATCH /workbooks/:workbookId` | [docs](https://reference.flatfile.com/api-reference/workbooks/update) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://reference.flatfile.com/api-reference/files/upload) |
| [Validate Sheet](actions/validate-sheet.md) | `POST /sheets/:sheetId/validate` | [docs](https://reference.flatfile.com/api-reference/sheets/validate) |
