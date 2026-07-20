# Bigin by Zoho CRM: Native API Reference

A consolidated summary of Bigin by Zoho CRM's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://www.bigin.com/developer/docs/apis/v2/
- **API base URL:** `{api_domain}/bigin/v2`

## Authentication

### OAuth2

OAuth2 authentication for Bigin by Zoho CRM APIs

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.accounts-server}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoBigin.users.ALL,ZohoBigin.org.ALL,ZohoBigin.settings.ALL,ZohoBigin.modules.ALL,ZohoBigin.bulk.ALL,ZohoBigin.notifications.ALL,ZohoBigin.coql.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.accounts-server}}/oauth/v2/token.

[Official authentication documentation](https://www.bigin.com/developer/docs/apis/v2/oauth-overview.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `modules`.

## Pagination

Use `per_page` in the query string to set the page size (default 200; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Notes](actions/add-notes.md) | `POST /Notes` | [docs](https://www.bigin.com/developer/docs/apis/v2/create-notes.html) |
| [Add Record Notes](actions/add-record-notes.md) | `POST /:module_api_name/:record_id/Notes` | [docs](https://www.bigin.com/developer/docs/apis/v2/create-notes.html) |
| [Add Records](actions/add-records.md) | `POST /:module_api_name` | [docs](https://www.bigin.com/developer/docs/apis/v2/insert-records.html) |
| [Count Records](actions/count-records.md) | `GET /:module_api_name/actions/count` | [docs](https://www.bigin.com/developer/docs/apis/v2/count-records.html) |
| [Delete Record](actions/delete-record.md) | `DELETE /:module_api_name/:record_id` | [docs](https://www.bigin.com/developer/docs/apis/v2/delete-records.html) |
| [Delete Records](actions/delete-records.md) | `DELETE /:module_api_name` | [docs](https://www.bigin.com/developer/docs/apis/v2/delete-records.html) |
| [Get Record](actions/get-record.md) | `GET /:module_api_name/:record_id` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-records.html) |
| [List Deleted Records](actions/list-deleted-records.md) | `GET /:module_api_name/deleted` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-deleted-records.html) |
| [List Fields](actions/list-fields.md) | `GET /settings/fields` | [docs](https://www.bigin.com/developer/docs/apis/v2/field-meta.html) |
| [List Modules](actions/list-modules.md) | `GET /settings/modules` | [docs](https://www.bigin.com/developer/docs/apis/v2/modules-api.html) |
| [List Notes](actions/list-notes.md) | `GET /Notes` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-notes.html) |
| [List Record Attachments](actions/list-record-attachments.md) | `GET /:moduleApiName/:recordId/Attachments` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-attachments.html) |
| [List Record Notes](actions/list-record-notes.md) | `GET /:moduleApiName/:recordId/Notes` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-notes.html) |
| [List Records](actions/list-records.md) | `GET /:module_api_name` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-records.html) |
| [List Related Records](actions/list-related-records.md) | `GET /:module_api_name/:record_id/:related_list_api_name` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-related-records.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-users.html) |
| [Run COQL Query](actions/run-coql-query.md) | `POST /coql` | [docs](https://www.bigin.com/developer/docs/apis/v2/get-records-using-coql-query.html) |
| [Search Records](actions/search-records.md) | `GET /:moduleApiName/search` | [docs](https://www.bigin.com/developer/docs/apis/v2/search-records.html) |
| [Update Record](actions/update-record.md) | `PUT /:module_api_name/:record_id` | [docs](https://www.bigin.com/developer/docs/apis/v2/update-records.html) |
| [Update Records](actions/update-records.md) | `PUT /:module_api_name` | [docs](https://www.bigin.com/developer/docs/apis/v2/update-records.html) |
| [Update Related Records](actions/update-related-records.md) | `PUT /:module_api_name/:record_id/:related_list_api_name` | [docs](https://www.bigin.com/developer/docs/apis/v2/update-related-records.html) |
| [Upsert Records](actions/upsert-records.md) | `POST /:module_api_name/upsert` | [docs](https://www.bigin.com/developer/docs/apis/v2/upsert-records.html) |
