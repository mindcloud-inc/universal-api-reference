# HiDrive: Native API Reference

A consolidated summary of HiDrive's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.hidrive.com/http-api-reference/
- **API base URL:** `https://api.hidrive.strato.com/2.1`

## Authentication

### OAuth 2

OAuth 2 authorization-code connection for the HiDrive HTTP API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://my.hidrive.com/client/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://my.hidrive.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `admin,rw`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://my.hidrive.com/oauth2/token.

[Official authentication documentation](https://developer.hidrive.com/oauth2-endpoints/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–5000).

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Directory](actions/copy-directory.md) | `POST /dir/copy` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/copy_POST) |
| [Copy File](actions/copy-file.md) | `POST /file/copy` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/copy_POST) |
| [Create Directory](actions/create-directory.md) | `POST /dir` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir_POST) |
| [Create Mail Upload](actions/create-mail-upload.md) | `POST /mailupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_POST) |
| [Create Share](actions/create-share.md) | `POST /share` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_POST) |
| [Create Share Link](actions/create-share-link.md) | `POST /sharelink` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink_POST) |
| [Create Share Upload](actions/create-share-upload.md) | `POST /shareupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/shareupload_POST) |
| [Delete Directory](actions/delete-directory.md) | `DELETE /dir` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir_DELETE) |
| [Delete File](actions/delete-file.md) | `DELETE /file` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file_DELETE) |
| [Delete Mail Upload](actions/delete-mail-upload.md) | `DELETE /mailupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_DELETE) |
| [Delete Share](actions/delete-share.md) | `DELETE /share` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_DELETE) |
| [Delete Share Link](actions/delete-share-link.md) | `DELETE /sharelink` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink_DELETE) |
| [Delete Share Upload](actions/delete-share-upload.md) | `DELETE /shareupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/shareupload_DELETE) |
| [Get App Info](actions/get-app-info.md) | `GET /app/me` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/app/me_GET) |
| [Get Current User](actions/get-current-user.md) | `GET /user/me` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/user/me_GET) |
| [Get Disabled Status](actions/get-disabled-status.md) | `GET /status/disabled` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/status/disabled_GET) |
| [Get Features](actions/get-features.md) | `GET /features` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/features_GET) |
| [Get File Download URL](actions/get-file-download-url.md) | `GET /file/url` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/url_GET) |
| [Get File Hashes](actions/get-file-hashes.md) | `GET /file/hash` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/hash_GET) |
| [Get Metadata](actions/get-metadata.md) | `GET /meta` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/meta_GET) |
| [Get Share Info](actions/get-share-info.md) | `GET /share/info` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share/info_GET) |
| [Get Share Link Info](actions/get-share-link-info.md) | `GET /sharelink/info` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink/info_GET) |
| [Get Unique Identifier](actions/get-unique-identifier.md) | `GET /unique` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/unique_GET) |
| [List Directory](actions/list-directory.md) | `GET /dir` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir_GET) |
| [List Home Directory](actions/list-home-directory.md) | `GET /dir/home` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/home_GET) |
| [List Mail Uploads](actions/list-mail-uploads.md) | `GET /mailupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_GET) |
| [List Share Links](actions/list-share-links.md) | `GET /sharelink` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink_GET) |
| [List Share Uploads](actions/list-share-uploads.md) | `GET /shareupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/shareupload_GET) |
| [List Shares](actions/list-shares.md) | `GET /share` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_GET) |
| [List Snapshots](actions/list-snapshots.md) | `GET /snapshot` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/snapshot_GET) |
| [Move Directory](actions/move-directory.md) | `POST /dir/move` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/move_POST) |
| [Move File](actions/move-file.md) | `POST /file/move` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/move_POST) |
| [Rename Directory](actions/rename-directory.md) | `POST /dir/rename` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/rename_POST) |
| [Rename File](actions/rename-file.md) | `POST /file/rename` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/rename_POST) |
| [Search Files](actions/search-files.md) | `GET /search` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/search_GET) |
| [Update Mail Upload](actions/update-mail-upload.md) | `PUT /mailupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_PUT) |
| [Update Metadata](actions/update-metadata.md) | `PATCH /meta` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/meta_PATCH) |
| [Update Share](actions/update-share.md) | `PUT /share` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_PUT) |
| [Update Share Link](actions/update-share-link.md) | `PUT /sharelink` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink_PUT) |
| [Update Share Upload](actions/update-share-upload.md) | `PUT /shareupload` | [docs](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/shareupload_PUT) |
