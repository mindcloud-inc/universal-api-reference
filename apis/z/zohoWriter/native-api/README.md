# Zoho Writer: Native API Reference

A consolidated summary of Zoho Writer's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/writer/help/api/v1/getting-started.html
- **API base URL:** `{api_domain}/writer/api`

## Authentication

### OAuth2

OAuth2 authentication for Zoho Writer APIs

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoWriter.documentEditor.ALL,ZohoWriter.merge.ALL,ZohoPC.files.ALL,WorkDrive.files.ALL,WorkDrive.organization.ALL,WorkDrive.workspace.ALL,WorkDrive.team.READ,ZohoSearch.securesearch.READ,ZohoSign.documents.ALL`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/writer/help/api/v1/oauth-2.html)

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `sortby` in the query string. Set the direction separately with `sort_order_by`. Use `ascending` for ascending order and `descending` for descending order. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Combine And Deliver Via Webhook](actions/combine-and-deliver-via-webhook.md) | `POST /v1/documents/pdf/combine/webhook` | [docs](https://www.zoho.com/writer/help/api/v1/combine-and-deliver-via-webhook.html) |
| [Combine And Store](actions/combine-and-store.md) | `POST /v1/documents/pdf/combine/store` | [docs](https://www.zoho.com/writer/help/api/v1/combine-and-store.html) |
| [Copy Document](actions/copy-document.md) | `POST /v1/documents/:document_id/copy` | [docs](https://www.zoho.com/writer/help/api/v1/copy-document.html) |
| [Create Template](actions/create-template.md) | `POST /v1/templates` | [docs](https://www.zoho.com/writer/help/api/v1/create-template.html) |
| [Create/Upload Documents](actions/create-upload-documents.md) | `POST /v1/documents` | [docs](https://www.zoho.com/writer/help/api/v1/create-upload-documents.html) |
| [Delete Document Permanently](actions/delete-document-permanently.md) | `DELETE /v1/documents/:document_id/delete` | [docs](https://www.zoho.com/writer/help/api/v1/delete-document-permanently.html) |
| [Download Document](actions/download-document.md) | `GET /v1/download/:document_id` | [docs](https://www.zoho.com/writer/help/api/v1/download-document.html) |
| [Enable Or Disable Track Changes](actions/enable-or-disable-track-changes.md) | `POST /v1/documents/:document_id/meta` | [docs](https://www.zoho.com/writer/help/api/v1/enable-or-disable-track-changes.html) |
| [Get All Fields](actions/get-all-fields.md) | `GET /v1/documents/:document_id/fields` | [docs](https://www.zoho.com/writer/help/api/v1/get-all-fields.html) |
| [Get Document Details](actions/get-document-details.md) | `GET /v1/documents/:document_id` | [docs](https://www.zoho.com/writer/help/api/v1/get-document-details.html) |
| [Get Document Metrics](actions/get-document-metrics.md) | `GET /v1/documents/:document_id/metrics` | [docs](https://www.zoho.com/writer/help/api/v1/get-document-metrics.html) |
| [Get Template Details](actions/get-template-details.md) | `GET /v1/templates/:template_id` | [docs](https://www.zoho.com/writer/help/api/v1/get-template-details.html) |
| [List Documents](actions/list-documents.md) | `GET /v1/documents` | [docs](https://www.zoho.com/writer/help/api/v1/get-list-of-documents.html) |
| [List Fillable Templates](actions/list-fillable-templates.md) | `GET /v1/documents` | [docs](https://www.zoho.com/writer/help/api/v1/get-fillable-templates.html) |
| [List Folders](actions/list-folders.md) | `GET /v1/folders` | [docs](https://www.zoho.com/writer/help/api/v1/get-list-of-folders.html) |
| [List Merge Templates](actions/list-merge-templates.md) | `GET /v1/documents` | [docs](https://www.zoho.com/writer/help/api/v1/get-merge-templates.html) |
| [List Sign Templates](actions/list-sign-templates.md) | `GET /v1/documents` | [docs](https://www.zoho.com/writer/help/api/v1/get-sign-templates.html) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://www.zoho.com/writer/help/api/v1/get-list-of-templates.html) |
| [Lock Or Unlock Document](actions/lock-or-unlock-document.md) | `POST /v1/documents/:document_id/meta` | [docs](https://www.zoho.com/writer/help/api/v1/lock-or-unlock-document.html) |
| [Merge And Email](actions/merge-and-email.md) | `POST /v1/documents/:document_id/merge/email` | [docs](https://www.zoho.com/writer/help/api/v1/inline-mail-merge-api.html) |
| [Merge and Store V2](actions/merge-and-store-v2.md) | `POST /v2/documents/:document_id/merge/store` | [docs](https://www.zoho.com/writer/help/api/v1/merge-and-store-v2.html) |
| [Merge Document](actions/merge-document.md) | `POST /v1/documents/:document_id/merge` | [docs](https://www.zoho.com/writer/help/api/v1/merge-document.html) |
| [Publish Document](actions/publish-document.md) | `POST /v1/documents/:document_id/publish` | [docs](https://www.zoho.com/writer/help/api/v1/publish-document.html) |
| [Rename Document](actions/rename-document.md) | `POST /v1/documents/:document_id/meta` | [docs](https://www.zoho.com/writer/help/api/v1/rename-document.html) |
| [Restore Document](actions/restore-document.md) | `POST /v1/documents/:document_id/restore` | [docs](https://www.zoho.com/writer/help/api/v1/restore-document.html) |
| [Search Documents](actions/search-documents.md) | `GET /v1/documents/search` | [docs](https://www.zoho.com/writer/help/api/v1/search-document.html) |
| [Trash Document](actions/trash-document.md) | `DELETE /v1/documents/:document_id/trash` | [docs](https://www.zoho.com/writer/help/api/v1/trash-document.html) |
| [Unpublish Document](actions/unpublish-document.md) | `DELETE /v1/documents/:document_id/publish` | [docs](https://www.zoho.com/writer/help/api/v1/unpublish-document.html) |
| [Update Document Description](actions/update-document-description.md) | `POST /v1/documents/:document_id/meta` | [docs](https://www.zoho.com/writer/help/api/v1/add-or-update-document-title.html) |
