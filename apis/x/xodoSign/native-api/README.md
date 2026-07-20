# Xodo Sign: Native API Reference

A consolidated summary of Xodo Sign's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://eversign.com/api/documentation
- **API base URL:** `https://api.eversign.com`

## Authentication

### API Key

Connect Xodo Sign with an API access key from the Developer page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://eversign.com/api/documentation/methods)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Audit Log](actions/audit-log.md) | `GET /document/:documentHash/audit_log` | [docs](https://eversign.com/api/documentation/methods#audit-log) |
| [Cancel Document](actions/cancel-document.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods#cancel-document) |
| [Create Bulk Job](actions/create-bulk-job.md) | `POST /template/:templateHash/bulk/job` | [docs](https://eversign.com/api/documentation/methods#create-bulk-job) |
| [Create Document](actions/create-document.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods#create-document) |
| [Create Template](actions/create-template.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods#create-template) |
| [Delete Document or Template](actions/delete-document-or-template.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods#delete-document) |
| [Download Final PDF](actions/download-final-pdf.md) | `GET /download_final_document` | [docs](https://eversign.com/api/documentation/methods#download-final-pdf) |
| [Download Original PDF](actions/download-original-pdf.md) | `GET /download_raw_document` | [docs](https://eversign.com/api/documentation/methods#download-original-pdf) |
| [Generate Blank Bulk CSV](actions/generate-blank-bulk-csv.md) | `GET /template/:templateHash/bulk/csv/blank` | [docs](https://eversign.com/api/documentation/methods#get-bulk-sending-blank-csv) |
| [Get Bulk Job](actions/get-bulk-job.md) | `GET /bulk_job/:bulkSendingJobId` | [docs](https://eversign.com/api/documentation/methods#get-bulk-job-by-id) |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | `GET /bulk_job/:bulkSendingJobId/status` | [docs](https://eversign.com/api/documentation/methods#get-bulk-job-status-by-id) |
| [Get Document or Template](actions/get-document-or-template.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods#get-document-template) |
| [List Bulk Job Documents](actions/list-bulk-job-documents.md) | `GET /bulk_job/:bulkSendingJobId/documents` | [docs](https://eversign.com/api/documentation/methods#get-bulk-job-documents-by-id) |
| [List Bulk Jobs](actions/list-bulk-jobs.md) | `GET /bulk_job` | [docs](https://eversign.com/api/documentation/methods#get-bulk-jobs-list) |
| [List Businesses](actions/list-businesses.md) | `GET /business` | [docs](https://eversign.com/api/documentation/methods#list-businesses) |
| [List Documents](actions/list-documents.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods#list-documents) |
| [List Templates](actions/list-templates.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods#list-templates) |
| [Reassign Signer](actions/reassign-signer.md) | `POST /reassign` | [docs](https://eversign.com/api/documentation/methods#reassign-signer) |
| [Send Reminder](actions/send-reminder.md) | `POST /send_reminder` | [docs](https://eversign.com/api/documentation/methods#send-reminder) |
| [Trash Document or Template](actions/trash-document-or-template.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods#trash-document) |
| [Upload File](actions/upload-file.md) | `POST /file` | [docs](https://eversign.com/api/documentation/methods#upload-file) |
| [Use Template](actions/use-template.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods#use-template) |
| [Validate Bulk Sending CSV](actions/validate-bulk-sending-csv.md) | `POST /template/:templateHash/bulk/csv/validate` | [docs](https://eversign.com/api/documentation/methods#validate-bulk-sending-csv) |
