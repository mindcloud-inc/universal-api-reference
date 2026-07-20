# Zoho Recruit: Native API Reference

A consolidated summary of Zoho Recruit's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/recruit/developer-guide/apiv2/
- **API base URL:** `https://recruit.zoho.com/recruit/v2`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoRecruit.modules.ALL,ZohoRecruit.settings.ALL,ZohoRecruit.users.ALL,ZohoRecruit.bulk.ALL`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/recruit/developer-guide/apiv2/oauth-overview.html)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags](actions/add-tags.md) | `POST /:moduleApiName/:recordId/actions/add_tags` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/add-tags.html) |
| [Create Notes](actions/create-notes.md) | `POST /Notes` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/create-notes.html) |
| [Create Records](actions/create-records.md) | `POST /:moduleApiName` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/insert-records.html) |
| [Delete Attachment](actions/delete-attachment.md) | `DELETE /:moduleApiName/:recordId/Attachments/:attachmentId` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/delete-attachments.html) |
| [Delete Note](actions/delete-note.md) | `DELETE /Notes/:noteId` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/delete-notes.html) |
| [Delete Records](actions/delete-records.md) | `DELETE /:moduleApiName` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/delete-records.html) |
| [Download Attachment](actions/download-attachment.md) | `GET /:moduleApiName/:recordId/Attachments/:attachmentId` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/download-attachments.html) |
| [Download Bulk Read Result](actions/download-bulk-read-result.md) | `GET https://recruit.zoho.com/recruit/bulk/v2/read/:jobId/result` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/bulk-read/download-result.html) |
| [Get Bulk Read Job Details](actions/get-bulk-read-job-details.md) | `GET https://recruit.zoho.com/recruit/bulk/v2/read/:jobId` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/bulk-read/job-details.html) |
| [Get Module](actions/get-module.md) | `GET /settings/modules/:moduleApiName` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/modules-api.html) |
| [Get Record](actions/get-record.md) | `GET /:moduleApiName/:recordId` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/get-records.html) |
| [Get Related Records](actions/get-related-records.md) | `GET /:moduleApiName/:recordId/:relatedModule` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/get-related-records.html) |
| [Initiate Bulk Read Job](actions/initiate-bulk-read-job.md) | `POST https://recruit.zoho.com/recruit/bulk/v2/read` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/bulk-read/create-job.html) |
| [List Custom Views](actions/list-custom-views.md) | `GET /settings/custom_views` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/custom-view-meta.html) |
| [List Fields](actions/list-fields.md) | `GET /settings/fields` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/field-meta.html) |
| [List Modules](actions/list-modules.md) | `GET /settings/modules` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/modules-api.html) |
| [List Notes](actions/list-notes.md) | `GET /Notes` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/get-notes.html) |
| [List Records](actions/list-records.md) | `GET /:moduleApiName` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/get-records.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/get-users.html) |
| [Remove Tags](actions/remove-tags.md) | `POST /:moduleApiName/:recordId/actions/remove_tags` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/remove-tags.html) |
| [Search Records](actions/search-records.md) | `GET /:moduleApiName/search` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/search-records.html) |
| [Update Records](actions/update-records.md) | `PUT /:moduleApiName` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/update-records.html) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /:moduleApiName/:recordId/Attachments` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/upload-attachment.html) |
| [Upsert Records](actions/upsert-records.md) | `POST /:moduleApiName/upsert` | [docs](https://www.zoho.com/recruit/developer-guide/apiv2/upsert-records.html) |
