# Kintone: Native API Reference

A consolidated summary of Kintone's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://kintone.dev/en/docs/kintone/rest-api/
- **API base URL:** `{baseUrl}/k/v1`

## Authentication

### OAuth 2.0

OAuth requires a tenant-specific Base URL, Configure users on the OAuth client, and no API IP restriction conflicts.

### Credentials

- **Base URL:** `baseUrl` · required · The full Kintone tenant URL, for example https://example.kintone.com. It must match the tenant where the configured OAuth client exists.
- **Client ID:** `clientId` · required · The OAuth client ID generated inside this Kintone tenant. It must belong to the same tenant as Base URL.
- **Client Secret:** `clientSecret` · required · The OAuth client secret generated for this Kintone tenant's OAuth client.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.baseUrl}}/oauth2/authorization to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.baseUrl}}/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `k:app_settings:read k:app_record:read k:app_record:write k:file:read k:file:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.baseUrl}}/oauth2/token.

[Official authentication documentation](https://kintone.dev/en/docs/common/authentication/how-to-add-oauth-clients/)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST /record/comment.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/add-comment/) |
| [Add Record](actions/add-record.md) | `POST /record.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/add-record/) |
| [Add Records](actions/add-records.md) | `POST /records.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/add-records/) |
| [Delete Records](actions/delete-records.md) | `DELETE /records.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/delete-records/) |
| [Download File](actions/download-file.md) | `GET /file.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/files/download-file/) |
| [Get Action Settings](actions/get-action-settings.md) | `GET /app/actions.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/settings/get-actions/) |
| [Get App](actions/get-app.md) | `GET /app.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/get-app/) |
| [Get App Permissions](actions/get-app-permissions.md) | `GET /app/acl.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/permissions/get-app-permissions/) |
| [Get Form](actions/get-form.md) | `GET /form.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/get-form/) |
| [Get Form Fields](actions/get-form-fields.md) | `GET /app/form/fields.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/form/get-form-fields/) |
| [Get Form Layout](actions/get-form-layout.md) | `GET /app/form/layout.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/form/get-form-layout/) |
| [Get General Settings](actions/get-general-settings.md) | `GET /app/settings.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/settings/get-general-settings/) |
| [Get Process Management Settings](actions/get-process-management-settings.md) | `GET /app/status.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/settings/get-process-management-settings/) |
| [Get Record](actions/get-record.md) | `GET /record.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/get-record/) |
| [Get Views](actions/get-views.md) | `GET /app/views.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/view/get-views/) |
| [List Apps](actions/list-apps.md) | `GET /apps.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/apps/get-apps/) |
| [List Comments](actions/list-comments.md) | `GET /record/comments.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/get-comments/) |
| [List Records](actions/list-records.md) | `GET /records.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/get-records/) |
| [Update Assignees](actions/update-assignees.md) | `PUT /record/assignees.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/update-assignees/) |
| [Update Record](actions/update-record.md) | `PUT /record.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/update-record/) |
| [Update Records](actions/update-records.md) | `PUT /records.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/update-records/) |
| [Update Status](actions/update-status.md) | `PUT /record/status.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/update-status/) |
| [Update Statuses](actions/update-statuses.md) | `PUT /records/status.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/records/update-statuses/) |
| [Upload File](actions/upload-file.md) | `POST /file.json` | [docs](https://kintone.dev/en/docs/kintone/rest-api/files/upload-file/) |
