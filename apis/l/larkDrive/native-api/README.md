# Lark Drive: Native API Reference

A consolidated summary of Lark Drive's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://open.larksuite.com/document
- **API base URL:** `https://open.larksuite.com/open-apis`

## Authentication

### Lark Custom App

Use Lark custom app credentials to request a tenant_access_token before calling Drive APIs.

### Credentials

- **App ID:** `appId` · required · Lark custom app app_id used to request tenant_access_token.
- **App Secret:** `appSecret` · required · Lark custom app app_secret used to request tenant_access_token.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://open.larksuite.com/document/server-docs/authentication-management/access-token/tenant_access_token_internal)

### OAuth2 User

Use Lark user authorization to access Drive resources in the signed-in user's context.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.larksuite.com/open-apis/authen/v1/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://open.larksuite.com/open-apis/authen/v2/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access auth:user.id:read drive:drive drive:drive:readonly drive:drive.metadata:readonly space:document:retrieve`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://open.larksuite.com/open-apis/authen/v2/oauth/token.

[Official authentication documentation](https://open.larksuite.com/document/common-capabilities/sso/api/obtain-oauth-code)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–200). Use `page_token` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check File Task](actions/check-file-task.md) | `GET /drive/v1/files/task_check` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/task_check) |
| [Copy File](actions/copy-file.md) | `POST /drive/v1/files/:file_token/copy` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/copy) |
| [Create Folder](actions/create-folder.md) | `POST /drive/v1/files/create_folder` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/create_folder) |
| [Delete File or Folder](actions/delete-file-or-folder.md) | `DELETE /drive/v1/files/:file_token` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/delete) |
| [Download File](actions/download-file.md) | `GET /drive/v1/files/:file_token/download` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/download) |
| [Get File Statistics](actions/get-file-statistics.md) | `GET /drive/v1/files/:file_token/statistics` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file-statistics/get) |
| [Get Root Folder Meta](actions/get-root-folder-meta.md) | `GET /drive/explorer/v2/root_folder/meta` | [docs](https://open.larksuite.com/document/ukTMukTMukTM/ugTNzUjL4UzM14CO1MTN/get-root-folder-meta) |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | `POST /auth/v3/tenant_access_token/internal` | [docs](https://open.larksuite.com/document/server-docs/authentication-management/access-token/tenant_access_token_internal) |
| [List Files](actions/list-files.md) | `GET /drive/v1/files` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/list) |
| [Move File or Folder](actions/move-file-or-folder.md) | `POST /drive/v1/files/:file_token/move` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/move) |
| [Refresh User Token](actions/refresh-user-token.md) | `POST /authen/v2/oauth/token` | [docs](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/authentication-management/access-token/refresh-user-access-token) |
