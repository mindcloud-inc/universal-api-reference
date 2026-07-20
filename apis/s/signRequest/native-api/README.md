# SignRequest: Native API Reference

A consolidated summary of SignRequest's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://signrequest.com/api/v1/docs/
- **OpenAPI specification:** https://signrequest.com/api/v1/schema/swagger.json
- **API base URL:** `https://signrequest.com/api/v1`

## Authentication

### OAuth2

Connect SignRequest with OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://signrequest.com/api/v1/oauth2/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to https://signrequest.com/api/v1/oauth2/token/.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://signrequest.com/api/v1/oauth2/token/.

[Official authentication documentation](https://signrequest.com/api/v1/docs/#section/Integration-Partners/OAuth2-Authorization-Framework)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel SignRequest](actions/cancel-sign-request.md) | `POST /signrequests/:uuid/cancel_signrequest/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequests_cancel_signrequest) |
| [Create Document](actions/create-document.md) | `POST /documents/` | [docs](https://signrequest.com/api/v1/docs/#operation/documents_create) |
| [Create Document Attachment](actions/create-document-attachment.md) | `POST /document-attachments/` | [docs](https://signrequest.com/api/v1/docs/#operation/document-attachments_create) |
| [Create SignRequest](actions/create-sign-request.md) | `POST /signrequests/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequests_create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/` | [docs](https://signrequest.com/api/v1/docs/#operation/webhooks_create) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/documents_delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/webhooks_delete) |
| [Forward SignRequest](actions/forward-sign-request.md) | `POST /signrequests/:uuid/forward_signer/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequests_forward_signer) |
| [Get Document](actions/get-document.md) | `GET /documents/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/documents_read) |
| [Get Document Attachment](actions/get-document-attachment.md) | `GET /document-attachments/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/document-attachments_read) |
| [Get SignRequest](actions/get-sign-request.md) | `GET /signrequests/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequests_read) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/webhooks_read) |
| [List Document Attachments](actions/list-document-attachments.md) | `GET /document-attachments/` | [docs](https://signrequest.com/api/v1/docs/#operation/document-attachments_list) |
| [List Documents](actions/list-documents.md) | `GET /documents/` | [docs](https://signrequest.com/api/v1/docs/#operation/documents_list) |
| [List Events](actions/list-events.md) | `GET /events/` | [docs](https://signrequest.com/api/v1/docs/#operation/events_list) |
| [List SignRequests](actions/list-sign-requests.md) | `GET /signrequests/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequests_list) |
| [List Templates](actions/list-templates.md) | `GET /templates/` | [docs](https://signrequest.com/api/v1/docs/#operation/templates_list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/` | [docs](https://signrequest.com/api/v1/docs/#operation/webhooks_list) |
| [Quick Create SignRequest](actions/quick-create-sign-request.md) | `POST /signrequest-quick-create/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequest-quick-create_create) |
| [Resend SignRequest](actions/resend-sign-request.md) | `POST /signrequests/:uuid/resend_signrequest_email/` | [docs](https://signrequest.com/api/v1/docs/#operation/signrequests_resend_signrequest_email) |
| [Search Documents](actions/search-documents.md) | `GET /documents-search/` | [docs](https://signrequest.com/api/v1/docs/#operation/documents-search_list) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:uuid/` | [docs](https://signrequest.com/api/v1/docs/#operation/webhooks_partial_update) |
