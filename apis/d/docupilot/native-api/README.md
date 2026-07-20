# Docupilot: Native API Reference

A consolidated summary of Docupilot's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.docupilot.app/developers/api-overview
- **OpenAPI specification:** https://api-us1.docupilot.app/dashboard/api/v2/schema/
- **API base URL:** `https://api.docupilot.app`

## Authentication

### API Key and Secret

Use a Docupilot API key, API secret, and workspace ID.

### Credentials

- **API Key:** `apiKey` · required · Docupilot API key from Settings > API Settings.
- **API Secret:** `apiSecret` · required · Docupilot API secret paired with the API key.
- **Workspace ID:** `workspaceId` · required · Workspace unique key used in the X-Workspace header for workspace APIs.

[Official authentication documentation](https://help.docupilot.app/developers/api-overview)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Template](actions/copy-template.md) | `POST /dashboard/api/v2/templates/{id}/copy/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Create Folder](actions/create-folder.md) | `POST /dashboard/api/v2/folders/` | [docs](https://help.docupilot.app/developers/folders-api) |
| [Create Template](actions/create-template.md) | `POST /dashboard/api/v2/templates/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Create Template Delivery](actions/create-template-delivery.md) | `POST /dashboard/api/v2/templates/{template_id}/deliveries/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Create Template Merge Link](actions/create-template-merge-link.md) | `POST /dashboard/api/v2/templates/{template_id}/merge_links/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /dashboard/api/v2/folders/{id}/` | [docs](https://help.docupilot.app/developers/folders-api) |
| [Delete Template](actions/delete-template.md) | `DELETE /dashboard/api/v2/templates/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Delete Template Delivery](actions/delete-template-delivery.md) | `DELETE /dashboard/api/v2/templates/{template_id}/deliveries/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Delete Template Merge Link](actions/delete-template-merge-link.md) | `DELETE /dashboard/api/v2/templates/{template_id}/merge_links/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Delete Template Permanently](actions/delete-template-permanently.md) | `DELETE /dashboard/api/v2/templates/{id}/permanent_delete/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Generate Document](actions/generate-document.md) | `POST /dashboard/api/v2/templates/{id}/generate/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Get Content Block](actions/get-content-block.md) | `GET /dashboard/api/v2/content_blocks/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Get Current Workspace](actions/get-current-workspace.md) | `GET /dashboard/accounts/v2/workspaces/current/` | [docs](https://help.docupilot.app/developers/api-overview) |
| [Get Template](actions/get-template.md) | `GET /dashboard/api/v2/templates/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Get Template Delivery](actions/get-template-delivery.md) | `GET /dashboard/api/v2/templates/{template_id}/deliveries/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Get Template Schema](actions/get-template-schema.md) | `GET /dashboard/api/v2/templates/{id}/schema/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Get Template Test Data](actions/get-template-test-data.md) | `GET /dashboard/api/v2/templates/{id}/test_data/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [List Content Blocks](actions/list-content-blocks.md) | `GET /dashboard/api/v2/content_blocks/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [List Folders](actions/list-folders.md) | `GET /dashboard/api/v2/folders/` | [docs](https://help.docupilot.app/developers/folders-api) |
| [List Generated Documents](actions/list-generated-documents.md) | `GET /dashboard/api/v2/history/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [List Template Deliveries](actions/list-template-deliveries.md) | `GET /dashboard/api/v2/templates/{template_id}/deliveries/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [List Template Merge Links](actions/list-template-merge-links.md) | `GET /dashboard/api/v2/templates/{template_id}/merge_links/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [List Templates](actions/list-templates.md) | `GET /dashboard/api/v2/templates/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [List Trashed Templates](actions/list-trashed-templates.md) | `GET /dashboard/api/v2/templates/trash/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Restore Template From Trash](actions/restore-template-from-trash.md) | `PUT /dashboard/api/v2/templates/{id}/restore/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Retry Document Delivery](actions/retry-document-delivery.md) | `POST /dashboard/api/v2/history/{id}/retry_delivery/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Update Folder](actions/update-folder.md) | `PUT /dashboard/api/v2/folders/{id}/` | [docs](https://help.docupilot.app/developers/folders-api) |
| [Update Template](actions/update-template.md) | `PUT /dashboard/api/v2/templates/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Update Template Content](actions/update-template-content.md) | `PATCH /dashboard/api/v2/templates/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
| [Update Template Delivery](actions/update-template-delivery.md) | `PUT /dashboard/api/v2/templates/{template_id}/deliveries/{id}/` | [docs](https://help.docupilot.app/developers/templates-api) |
