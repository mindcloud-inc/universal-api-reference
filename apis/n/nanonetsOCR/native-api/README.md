# Nanonets OCR: Native API Reference

A consolidated summary of Nanonets OCR's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.nanonets.com/docs/
- **API base URL:** `https://app.nanonets.com/api/v4`

## Authentication

### API Key

Authenticate with your Nanonets API key using HTTP Basic Auth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.nanonets.com/docs/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [Delete Document](actions/delete-document.md) | `DELETE /workflows/:workflow_id/documents/:document_id` | [docs](https://apidocs.nanonets.com/docs/api/document-processing/) |
| [Delete Field Or Table Header](actions/delete-field-or-table-header.md) | `DELETE /workflows/:workflow_id/fields/:field_id` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [Get Document Data](actions/get-document-data.md) | `GET /workflows/:workflow_id/documents/:document_id` | [docs](https://apidocs.nanonets.com/docs/api/document-processing/) |
| [Get Page Data](actions/get-page-data.md) | `GET /workflows/:workflow_id/documents/:document_id/pages/:page_id` | [docs](https://apidocs.nanonets.com/docs/api/document-processing/) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflow_id` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [List Available Workflow Types](actions/list-available-workflow-types.md) | `GET /workflow_types` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [List Documents](actions/list-documents.md) | `GET /workflows/:workflow_id/documents` | [docs](https://apidocs.nanonets.com/docs/api/document-processing/) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [Set Fields And Table Headers](actions/set-fields-and-table-headers.md) | `PUT /workflows/:workflow_id/fields` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [Update Field Or Table Header](actions/update-field-or-table-header.md) | `PATCH /workflows/:workflow_id/fields/:field_id` | [docs](https://apidocs.nanonets.com/docs/api/workflow-management/) |
| [Upload Document For Processing](actions/upload-document-for-processing.md) | `POST /workflows/:workflow_id/documents` | [docs](https://apidocs.nanonets.com/docs/api/document-processing/) |
