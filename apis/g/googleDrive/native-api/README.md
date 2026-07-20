# Google Drive: Native API Reference

A consolidated summary of Google Drive's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/drive/api/reference/rest/v3
- **OpenAPI specification:** https://github.com/APIs-guru/openapi-directory/blob/main/APIs/googleapis.com/drive/v3/openapi.yaml
- **API base URL:** `https://www.googleapis.com`

## Authentication

### OAuth 2.0

Create / Delete / Modify ALL Drive Files

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/drive.file https://www.googleapis.com/auth/drive.metadata.readonly`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/drive/api/guides/about-sdk)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–100). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | `POST /drive/v3/files/:fileId/copy` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/copy) |
| [Create File](actions/create-file.md) | `POST /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/create) |
| [Create Folder](actions/create-folder.md) | `POST /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/create) |
| [Export File](actions/export-file.md) | `GET /drive/v3/files/:fileId/export` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/export) |
| [Get Drive User (Auth)](actions/get-drive-user-auth.md) | `GET /drive/v3/about` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/about/get) |
| [Get Parent Folder](actions/get-parent-folder.md) | `GET /drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/get) |
| [List Documents](actions/list-documents.md) | `GET /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [List Files](actions/list-files.md) | `GET /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [List Folders](actions/list-folders.md) | `GET /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [List Shared Drives](actions/list-shared-drives.md) | `GET /drive/v3/drives` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/drives/list) |
| [List Spreadsheets](actions/list-spreadsheets.md) | `GET /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [Move File](actions/move-file.md) | `PATCH /drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/update) |
| [Search Files and Folders](actions/search-files-and-folders.md) | `GET /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
