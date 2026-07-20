# Scanova: Native API Reference

A consolidated summary of Scanova's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.scanova.io/
- **API base URL:** `https://management.scanova.io`

## Authentication

### API Key

Use a Scanova management API key. Scanova expects the raw API key in the Authorization header without a Bearer prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.scanova.io/api-reference/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Account Statistics](actions/account-statistics.md) | `GET /auth/stats/` | [docs](https://docs.scanova.io/api-reference/endpoint/analytics/stats) |
| [Add New User](actions/add-new-user.md) | `POST /multi-users/` | [docs](https://docs.scanova.io/api-reference/endpoint/user_management/add) |
| [Attach Or Detach Lead List](actions/attach-or-detach-lead-list.md) | `PATCH /qr/{qrid}/` | [docs](https://docs.scanova.io/api-reference/endpoint/lead_list/attach) |
| [Create QR Code](actions/create-qr-code.md) | `POST /qr/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/create) |
| [Create Tag](actions/create-tag.md) | `POST /tag/list/` | [docs](https://docs.scanova.io/) |
| [Delete Lead List](actions/delete-lead-list.md) | `DELETE /lead/{lead_list_id}/` | [docs](https://docs.scanova.io/api-reference/endpoint/lead_list/delete) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qr/{qrid}/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/delete) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/{tag_id}/` | [docs](https://docs.scanova.io/) |
| [Download QR Code](actions/download-qr-code.md) | `GET /qr/{qrid}/download/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/download) |
| [Download QR Code (Printable)](actions/download-qr-code-printable.md) | `POST /qr/download/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/download-printable) |
| [Export Analytics Data](actions/export-analytics-data.md) | `POST /analytics/qr/export/` | [docs](https://docs.scanova.io/api-reference/endpoint/analytics/export) |
| [Export Raw Scan Data](actions/export-raw-scan-data.md) | `POST /analytics/qr/raw/` | [docs](https://docs.scanova.io/api-reference/endpoint/analytics/export-raw) |
| [Get QR Code Analytics](actions/get-qr-code-analytics.md) | `POST /analytics/qr/` | [docs](https://docs.scanova.io/api-reference/endpoint/analytics/qr-code) |
| [Get QR Code Categories](actions/get-qr-code-categories.md) | `GET /qr/category/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/categories) |
| [Get QR Code List](actions/get-qr-code-list.md) | `GET /qr/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/get) |
| [Get Tags](actions/get-tags.md) | `GET /tag/list/` | [docs](https://docs.scanova.io/) |
| [Get Trash QR Codes](actions/get-trash-qr-codes.md) | `GET /qr/trash/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/trash) |
| [Get User Details](actions/get-user-details.md) | `GET /multi-users/{shared-user-id}/` | [docs](https://docs.scanova.io/api-reference/endpoint/user_management/retrieve) |
| [Get User List](actions/get-user-list.md) | `GET /multi-users/` | [docs](https://docs.scanova.io/api-reference/endpoint/user_management/list) |
| [Get User Roles List](actions/get-user-roles-list.md) | `GET /multi-users/access-levels/` | [docs](https://docs.scanova.io/api-reference/endpoint/user_management/roles) |
| [List Lead Lists](actions/list-lead-lists.md) | `GET /lead/` | [docs](https://docs.scanova.io/api-reference/endpoint/lead_list/list) |
| [Permanently Delete QR Code](actions/permanently-delete-qr-code.md) | `DELETE /qrcode/trash/{qrid}/permanent-delete/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/trash) |
| [Remove User](actions/remove-user.md) | `DELETE /multi-users/{shared-user-id}/` | [docs](https://docs.scanova.io/api-reference/endpoint/user_management/remove) |
| [Restore QR Code From Trash](actions/restore-qr-code-from-trash.md) | `POST /qrcode/trash/{qrid}/restore/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/trash) |
| [Retrieve Lead List](actions/retrieve-lead-list.md) | `GET /lead/{lead_list_id}/` | [docs](https://docs.scanova.io/api-reference/endpoint/lead_list/retrieve) |
| [Update Lead List](actions/update-lead-list.md) | `PATCH /lead/{lead_list_id}/` | [docs](https://docs.scanova.io/api-reference/endpoint/lead_list/update) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /qr/{qrid}/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/update) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/{tag_id}/` | [docs](https://docs.scanova.io/) |
| [Update User Role](actions/update-user-role.md) | `PATCH /multi-users/{shared-user-id}/` | [docs](https://docs.scanova.io/api-reference/endpoint/user_management/update-role) |
| [Validate QR Code Info Data](actions/validate-qr-code-info-data.md) | `POST /qr/validate-info/` | [docs](https://docs.scanova.io/api-reference/endpoint/qr_manager/validate-info) |
