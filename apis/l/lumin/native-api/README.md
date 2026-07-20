# Lumin: Native API Reference

A consolidated summary of Lumin's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://developers.luminpdf.com/api/lumin-api-reference/
- **OpenAPI specification:** https://raw.githubusercontent.com/luminpdf/luminsign-docs/main/openapi.yaml
- **API base URL:** `https://api.luminpdf.com/v1`

## Authentication

### API Key

Connect Lumin with an API key from Developer Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://developers.luminpdf.com/docs/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `user`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 10–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Signature Request](actions/cancel-signature-request.md) | `PUT /signature_request/cancel/:signature_request_id` | [docs](https://developers.luminpdf.com/api/cancel-signature-request/) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://developers.luminpdf.com/api/create-document/) |
| [Download File](actions/download-file.md) | `GET /signature_request/files/:signature_request_id` | [docs](https://developers.luminpdf.com/api/download-file/) |
| [Download File As File URL](actions/download-file-as-file-url.md) | `GET /signature_request/files_as_file_url/:signature_request_id` | [docs](https://developers.luminpdf.com/api/download-file-as-file-url/) |
| [Get Signature Request](actions/get-signature-request.md) | `GET /signature_request/:signature_request_id` | [docs](https://developers.luminpdf.com/api/get-signature-request/) |
| [Get Signature Request File](actions/get-signature-request-file.md) | `GET /signature_request/:signature_request_id/file` | [docs](https://developers.luminpdf.com/api/get-signature-request-file/) |
| [Get Signing Link](actions/get-signing-link.md) | `POST /signature_request/:signature_request_id/signing-link` | [docs](https://developers.luminpdf.com/api/get-signing-link/) |
| [Get User Information](actions/get-user-information.md) | `GET /user/info` | [docs](https://developers.luminpdf.com/api/get-user-information/) |
| [Get Workspace Information](actions/get-workspace-information.md) | `GET /workspaces/info` | [docs](https://developers.luminpdf.com/api/get-workspace-information/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.luminpdf.com/api/list-templates/) |
| [List Workspace Members](actions/list-workspace-members.md) | `GET /workspaces/members` | [docs](https://developers.luminpdf.com/api/get-workspace-members/) |
| [Send Reminder Emails](actions/send-reminder-emails.md) | `POST /signature_request/remind/:signature_request_id` | [docs](https://developers.luminpdf.com/api/send-reminder-emails/) |
| [Send Signature Request](actions/send-signature-request.md) | `POST /signature_request/send` | [docs](https://developers.luminpdf.com/api/send-signature-request/) |
| [Update Signature Request](actions/update-signature-request.md) | `PATCH /signature_request/:signature_request_id` | [docs](https://developers.luminpdf.com/api/update-signature-request/) |
