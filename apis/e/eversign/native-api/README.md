# Eversign: Native API Reference

A consolidated summary of Eversign's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://eversign.com/api/documentation/methods
- **API base URL:** `https://api.eversign.com`

## Authentication

### API Key

Connect using an Eversign API access key and workspace business ID.

### Credentials

- **API Key:** `apiKey` · required
- **Business ID:** `businessId` · required · Numeric workspace business_id returned by the List Businesses API method.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://eversign.com/api/documentation/methods)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Audit Log](actions/audit-log.md) | `GET /document/:documentHash/audit_log` | [docs](https://eversign.com/api/documentation/methods) |
| [Cancel Document](actions/cancel-document.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Create Draft Document](actions/create-draft-document.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Create Embedded Document](actions/create-embedded-document.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Create My Action Document](actions/create-my-action-document.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Create Sandbox Document](actions/create-sandbox-document.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Create Template](actions/create-template.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Create Template Draft](actions/create-template-draft.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Delete Document](actions/delete-document.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Delete Template](actions/delete-template.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Download Document PDF](actions/download-document-pdf.md) | `GET /download_raw_document` | [docs](https://eversign.com/api/documentation/methods) |
| [Download Final PDF](actions/download-final-pdf.md) | `GET /download_final_document` | [docs](https://eversign.com/api/documentation/methods) |
| [Download Template PDF](actions/download-template-pdf.md) | `GET /download_raw_document` | [docs](https://eversign.com/api/documentation/methods) |
| [Generate Blank CSV](actions/generate-blank-csv.md) | `GET /template/:templateHash/bulk/csv/blank` | [docs](https://eversign.com/api/documentation/methods) |
| [Get Document](actions/get-document.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Get Template](actions/get-template.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List Bulk Jobs](actions/list-bulk-jobs.md) | `GET /bulk_job` | [docs](https://eversign.com/api/documentation/methods) |
| [List Businesses](actions/list-businesses.md) | `GET /business` | [docs](https://eversign.com/api/documentation/methods) |
| [List Cancelled Documents](actions/list-cancelled-documents.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List Documents](actions/list-documents.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List Draft Documents](actions/list-draft-documents.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List My Action Required Documents](actions/list-my-action-required-documents.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List Template Drafts](actions/list-template-drafts.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List Templates](actions/list-templates.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [List Waiting For Others Documents](actions/list-waiting-for-others-documents.md) | `GET /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Reassign Signer](actions/reassign-signer.md) | `POST /reassign` | [docs](https://eversign.com/api/documentation/methods) |
| [Send Reminder](actions/send-reminder.md) | `POST /send_reminder` | [docs](https://eversign.com/api/documentation/methods) |
| [Trash Document](actions/trash-document.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Trash Template](actions/trash-template.md) | `DELETE /document` | [docs](https://eversign.com/api/documentation/methods) |
| [Use Template](actions/use-template.md) | `POST /document` | [docs](https://eversign.com/api/documentation/methods) |
