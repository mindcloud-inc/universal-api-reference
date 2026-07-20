# SignWell: Native API Reference

A consolidated summary of SignWell's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.signwell.com/reference
- **API base URL:** `https://www.signwell.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://help.signwell.com/article/133-managing-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Completed PDF](actions/completed-pdf.md) | `GET /documents/:id/completed_pdf` | [docs](https://developers.signwell.com/reference/get_api-v1-documents-id-completed-pdf-1) |
| [Create Bulk Send](actions/create-bulk-send.md) | `POST /bulk_sends` | [docs](https://developers.signwell.com/reference/post_api-v1-bulk-sends) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://developers.signwell.com/reference/post_api-v1-documents) |
| [Create Document from Template](actions/create-document-from-template.md) | `POST /document_templates/documents` | [docs](https://developers.signwell.com/reference/post_api-v1-document-templates-documents) |
| [Create Template](actions/create-template.md) | `POST /document_templates` | [docs](https://developers.signwell.com/reference/post_api-v1-template) |
| [Create Webhook](actions/create-webhook.md) | `POST /hooks/` | [docs](https://developers.signwell.com/reference/post_api-v1-hooks-1) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:id` | [docs](https://developers.signwell.com/reference/delete_api-v1-documents-id) |
| [Delete Template](actions/delete-template.md) | `DELETE /document_templates/:id` | [docs](https://developers.signwell.com/reference/delete_api-v1-document-templates-id) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /hooks/:id/` | [docs](https://developers.signwell.com/reference/delete_api-v1-hooks-id) |
| [Get Bulk Send](actions/get-bulk-send.md) | `GET /bulk_sends/:id` | [docs](https://developers.signwell.com/reference/get_api-v1-bulk-sends-id) |
| [Get Bulk Send CSV Template](actions/get-bulk-send-csv-template.md) | `GET /bulk_sends/csv_template` | [docs](https://developers.signwell.com/reference/get_api-v1-bulk-sends-csv-template) |
| [Get Bulk Send Documents](actions/get-bulk-send-documents.md) | `GET /bulk_sends/:id/documents` | [docs](https://developers.signwell.com/reference/get_api-v1-bulk-sends-id-documents) |
| [Get Credentials](actions/get-credentials.md) | `GET /me` | [docs](https://developers.signwell.com/reference/get_api-v1-me) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://developers.signwell.com/reference/get_api-v1-documents-id) |
| [Get Template](actions/get-template.md) | `GET /document_templates/:id` | [docs](https://developers.signwell.com/reference/get_api-v1-document-templates-id) |
| [List Bulk Sendings](actions/list-bulk-sendings.md) | `GET /bulk_sends` | [docs](https://developers.signwell.com/reference/get_api-v1-bulk-sends) |
| [List Webhooks](actions/list-webhooks.md) | `GET /hooks/` | [docs](https://developers.signwell.com/reference/get_api-v1-hooks-1) |
| [Send Reminder](actions/send-reminder.md) | `POST /documents/:id/remind` | [docs](https://developers.signwell.com/reference/post_api-v1-documents-id-remind) |
| [Update and Send Document](actions/update-and-send-document.md) | `POST /documents/:id/send` | [docs](https://developers.signwell.com/reference/post_api-v1-documents-id-send) |
| [Update Recipients](actions/update-recipients.md) | `PATCH /documents/:id/recipients` | [docs](https://developers.signwell.com/reference/updaterecipients) |
| [Update Template](actions/update-template.md) | `PUT /document_templates/:id` | [docs](https://developers.signwell.com/reference/put_api-v1-document-templates-id) |
