# Google Docs: Native API Reference

A consolidated summary of Google Docs's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/docs/api/reference/rest
- **API base URL:** `https://docs.googleapis.com/v1/documents`

## Authentication

### OAuth 2.0

This action uses the Google Drive `drive.file` scope, so it only lists documents that were created by MindCloud or that the user has explicitly opened with MindCloud. If you need to browse a wider list of spreadsheets from Google Drive, use the Google Drive app instead.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/documents https://www.googleapis.com/auth/drive.file`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Retry behavior

Wait 60000 ms before the first retry. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Blank Document](actions/create-blank-document.md) | `POST /` | [docs](https://developers.google.com/workspace/docs/api/reference/rest/v1/documents/create) |
| [Delete Document](actions/delete-document.md) | `DELETE https://www.googleapis.com/drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/delete) |
| [Get Document](actions/get-document.md) | `GET /:documentId` | [docs](https://developers.google.com/workspace/docs/api/reference/rest/v1/documents/get) |
| [Insert Text](actions/insert-text.md) | `POST /[:documentId]\:batchUpdate` | [docs](https://developers.google.com/workspace/docs/api/reference/rest/v1/documents/batchUpdate) |
| [List Documents](actions/list-documents.md) | `GET https://www.googleapis.com/drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [Replace All Text](actions/replace-all-text.md) | `POST /[:documentId]\:batchUpdate` | [docs](https://developers.google.com/workspace/docs/api/reference/rest/v1/documents/batchUpdate) |
