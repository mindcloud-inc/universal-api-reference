# PixelBin.io: Native API Reference

A consolidated summary of PixelBin.io's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.pixelbin.io/docs/api/
- **API base URL:** `https://api.pixelbin.io`

## Authentication

### API Token

Use a PixelBin API token. MindCloud base64-encodes the raw token into the Authorization bearer header required by PixelBin platform routes.

### Credentials

- **API Token:** `apiToken` · required · Raw PixelBin API token from the dashboard Tokens page.

[Official authentication documentation](https://www.pixelbin.io/docs/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page.current`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Transformation Module Credentials](actions/add-credentials.md) | `POST /service/platform/assets/v1.0/credentials` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Add Preset](actions/add-preset.md) | `POST /service/platform/assets/v1.0/presets` | [docs](https://www.pixelbin.io/docs/presets/) |
| [Create Folder](actions/create-folder.md) | `POST /service/platform/assets/v1.0/folders` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Create Signed URL](actions/create-signed-url.md) | `POST /service/platform/assets/v1.0/upload/signed-url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
| [Create Signed URL V2](actions/create-signed-url-v2.md) | `POST /service/platform/assets/v2.0/upload/signed-url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
| [Delete Transformation Module Credentials](actions/delete-credentials.md) | `DELETE /service/platform/assets/v1.0/credentials/:pluginId` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Delete File](actions/delete-file.md) | `DELETE /service/platform/assets/v1.0/files/:fileId` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Delete Files](actions/delete-files.md) | `POST /service/platform/assets/v1.0/files/delete` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /service/platform/assets/v1.0/folders/:_id` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Delete Preset](actions/delete-preset.md) | `DELETE /service/platform/assets/v1.0/presets/:presetName` | [docs](https://www.pixelbin.io/docs/presets/) |
| [Upload File](actions/file-upload.md) | `POST /service/platform/assets/v1.0/upload/direct` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
| [Get App Org Details](actions/get-app-org-details.md) | `GET /service/platform/organization/v1.0/apps/info` | [docs](https://www.pixelbin.io/docs/organization/) |
| [Get Current Usage](actions/get-current-usage.md) | `GET /service/platform/payment/v1.0/usage` | [docs](https://www.pixelbin.io/docs/billing-and-payments/) |
| [Get Default Asset For Playground](actions/get-default-asset-for-playground.md) | `GET /service/platform/assets/v1.0/playground/default` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Get File By File ID](actions/get-file-by-file-id.md) | `GET /service/platform/assets/v1.0/files/:fileId` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [Get File By ID](actions/get-file-by-id.md) | `GET /service/platform/assets/v1.0/files/id/:_id` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [Get Folder Ancestors](actions/get-folder-ancestors.md) | `GET /service/platform/assets/v1.0/folders/:_id/ancestors` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Get Folder Details](actions/get-folder-details.md) | `GET /service/platform/assets/v1.0/folders` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [Get Preset](actions/get-preset.md) | `GET /service/platform/assets/v1.0/presets/:presetName` | [docs](https://www.pixelbin.io/docs/presets/) |
| [Get Subscription Usage](actions/get-subscription-usage.md) | `GET /service/platform/payment/v1.0/usage/subscription` | [docs](https://www.pixelbin.io/docs/billing-and-payments/) |
| [Get Transformation Context](actions/get-transformation-context.md) | `GET /service/platform/transformation/context` | [docs](https://www.pixelbin.io/docs/context/) |
| [Get Transformation Module](actions/get-transformation-module.md) | `GET /service/platform/assets/v1.0/playground/plugins/:identifier` | [docs](https://www.pixelbin.io/docs/playground/) |
| [List Files](actions/list-files.md) | `GET /service/platform/assets/v1.0/listFiles` | [docs](https://www.pixelbin.io/docs/storage/search/) |
| [List Presets](actions/list-presets.md) | `GET /service/platform/assets/v1.0/presets` | [docs](https://www.pixelbin.io/docs/presets/) |
| [List Transformation Modules](actions/list-transformation-modules.md) | `GET /service/platform/assets/v1.0/playground/plugins` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Update Transformation Module Credentials](actions/update-credentials.md) | `PATCH /service/platform/assets/v1.0/credentials/:pluginId` | [docs](https://www.pixelbin.io/docs/playground/) |
| [Update File](actions/update-file.md) | `PATCH /service/platform/assets/v1.0/files/:fileId` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Update Folder](actions/update-folder.md) | `PATCH /service/platform/assets/v1.0/folders/:folderId` | [docs](https://www.pixelbin.io/docs/storage/miscellaneous/) |
| [Update Preset](actions/update-preset.md) | `PATCH /service/platform/assets/v1.0/presets/:presetName` | [docs](https://www.pixelbin.io/docs/presets/) |
| [Upload Asset From URL](actions/url-upload.md) | `POST /service/platform/assets/v1.0/upload/url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
