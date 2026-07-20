# Feishu Drive: Native API Reference

A consolidated summary of Feishu Drive's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/file-overview
- **API base URL:** `https://open.feishu.cn/open-apis`

## Authentication

### Feishu Custom App

Use Feishu Custom App credentials to exchange app credentials for a tenant_access_token before calling Drive APIs.

### Credentials

- **App ID:** `appId` · required · Feishu Custom App app_id used to request tenant_access_token.
- **App Secret:** `appSecret` · required · Feishu Custom App app_secret used to request tenant_access_token.

Send these headers with each API request:

```http
Authorization: Bearer <custom.tenantAccessToken>
```

[Official authentication documentation](https://open.feishu.cn/document/server-docs/authentication-management/access-token/tenant_access_token_internal)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check File Task](actions/check-file-task.md) | `GET /drive/v1/files/task_check` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/task_check) |
| [Copy File](actions/copy-file.md) | `POST /drive/v1/files/:file_token/copy` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/copy) |
| [Create File Shortcut](actions/create-file-shortcut.md) | `POST /drive/v1/files/create_shortcut` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/create_shortcut) |
| [Create Folder](actions/create-folder.md) | `POST /drive/v1/files/create_folder` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/create_folder) |
| [Delete File or Folder](actions/delete-file-or-folder.md) | `DELETE /drive/v1/files/:file_token` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/delete) |
| [Download File](actions/download-file.md) | `GET /drive/v1/files/:file_token/download` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/download) |
| [Get File Metadata](actions/get-file-metadata.md) | `POST /drive/v1/metas/batch_query` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/meta/batch_query) |
| [Get File Statistics](actions/get-file-statistics.md) | `GET /drive/v1/files/:file_token/statistics` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file-statistics/get) |
| [Get Root Folder Meta](actions/get-root-folder-meta.md) | `GET /drive/explorer/v2/root_folder/meta` | [docs](https://open.feishu.cn/document/ukTMukTMukTM/ugTNzUjL4UzM14CO1MTN/get-root-folder-meta) |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | `POST /auth/v3/tenant_access_token/internal` | [docs](https://open.feishu.cn/document/server-docs/authentication-management/access-token/tenant_access_token_internal) |
| [List Files](actions/list-files.md) | `GET /drive/v1/files` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/list) |
| [Move File or Folder](actions/move-file-or-folder.md) | `POST /drive/v1/files/:file_token/move` | [docs](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/move) |
