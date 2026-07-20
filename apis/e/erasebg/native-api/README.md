# Erase.bg: Native API Reference

A consolidated summary of Erase.bg's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://www.erase.bg/g/api/remove-background
- **API base URL:** `https://api.pixelbin.io`

## Authentication

### API Token + Access Token

Authenticate Erase.bg requests with a base64-encoded API token plus a request signature

### Credentials

- **API Token:** `apiToken` · required · API token copied from the Erase.bg dashboard token flow
- **Access Token:** `accessToken` · required · Signing token used for PixelBin request signatures in this Stage 1 run

[Official authentication documentation](https://www.erase.bg/g/api/remove-background)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /service/platform/assets/v1.0/folders` | [docs](https://www.pixelbin.io/docs/storage/create-folder/) |
| [Create Signed Multipart Upload URL](actions/create-signed-multipart-upload-url.md) | `POST /service/platform/assets/v2.0/upload/signed-url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
| [Create Signed Upload URL](actions/create-signed-upload-url.md) | `POST /service/platform/assets/v1.0/upload/signed-url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
| [Delete File](actions/delete-file.md) | `DELETE /service/platform/assets/v1.0/files/:fileId` | [docs](https://www.pixelbin.io/docs/storage/delete-files/) |
| [Delete Files](actions/delete-files.md) | `POST /service/platform/assets/v1.0/files/delete` | [docs](https://www.pixelbin.io/docs/storage/delete-files/) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /service/platform/assets/v1.0/folders/:_id` | [docs](https://www.pixelbin.io/docs/storage/delete-files/) |
| [Get App Details](actions/get-app-details.md) | `GET /service/platform/organization/v1.0/apps/info` | [docs](https://www.pixelbin.io/docs/api/) |
| [Get Current Usage](actions/get-current-usage.md) | `GET /service/platform/payment/v1.0/usage` | [docs](https://www.pixelbin.io/docs/api/) |
| [Get Default Asset For Playground](actions/get-default-asset-for-playground.md) | `GET /service/platform/assets/v1.0/playground/default` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Get File By File ID](actions/get-file-by-file-id.md) | `GET /service/platform/assets/v1.0/files/:fileId` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [Get File By ID](actions/get-file-by-id.md) | `GET /service/platform/assets/v1.0/files/id/:_id` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [Get Folder Ancestors](actions/get-folder-ancestors.md) | `GET /service/platform/assets/v1.0/folders/:_id/ancestors` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Get Folder Details](actions/get-folder-details.md) | `GET /service/platform/assets/v1.0/folders` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Get Transformation Module](actions/get-transformation-module.md) | `GET /service/platform/assets/v1.0/playground/plugins/:identifier` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Get Transformation Modules](actions/get-transformation-modules.md) | `GET /service/platform/assets/v1.0/playground/plugins` | [docs](https://www.pixelbin.io/docs/playground/) |
| [List Files](actions/list-files.md) | `GET /service/platform/assets/v1.0/listFiles` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [Update File](actions/update-file.md) | `PATCH /service/platform/assets/v1.0/files/:fileId` | [docs](https://www.pixelbin.io/docs/storage/rename-file/) |
| [Update Folder](actions/update-folder.md) | `PATCH /service/platform/assets/v1.0/folders/:folderId` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Upload Asset From URL](actions/upload-asset-from-url.md) | `POST /service/platform/assets/v1.0/upload/url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
