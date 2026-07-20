# Uploadcare: Native API Reference

A consolidated summary of Uploadcare's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://uploadcare.com/api-refs/rest-api/v0.7.0/
- **API base URL:** `https://api.uploadcare.com`

## Authentication

### Uploadcare.Simple

Authenticate Uploadcare REST API requests with public and secret keys.

### Credentials

- **Public Key:** `publicKey` · required · Uploadcare project public API key.

[Official authentication documentation](https://uploadcare.com/docs/api/rest/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.uploadcare-v0.7+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000).

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Delete Files](actions/batch-delete-files.md) | `DELETE /files/storage/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/filesDelete) |
| [Batch Store Files](actions/batch-store-files.md) | `PUT /files/storage/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/filesStoring) |
| [Convert Document](actions/convert-document.md) | `POST /convert/document/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/documentConvert) |
| [Convert Video](actions/convert-video.md) | `POST /convert/video/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/videoConvert) |
| [Copy File To Local Storage](actions/copy-file-to-local-storage.md) | `POST /files/local_copy/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/createLocalCopy) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/webhookCreate) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:uuid/storage/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/deleteFileStorage) |
| [Delete File Metadata Key](actions/delete-file-metadata-key.md) | `DELETE /files/:uuid/metadata/:key/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/deleteFileMetadataKey) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:uuid/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Group/operation/deleteGroup) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/unsubscribe/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/webhookUnsubscribe) |
| [Get Document Conversion Info](actions/get-document-conversion-info.md) | `GET /convert/document/:uuid/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/documentConvertInfo) |
| [Get Document Conversion Status](actions/get-document-conversion-status.md) | `GET /convert/document/status/:token/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/documentConvertStatus) |
| [Get File](actions/get-file.md) | `GET /files/:uuid/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/fileInfo) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /files/:uuid/metadata/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/_fileMetadata) |
| [Get File Metadata Value](actions/get-file-metadata-value.md) | `GET /files/:uuid/metadata/:key/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/fileMetadataKey) |
| [Get Group](actions/get-group.md) | `GET /groups/:uuid/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Group/operation/groupInfo) |
| [Get Project](actions/get-project.md) | `GET /project/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Project/operation/projectInfo) |
| [List Files](actions/list-files.md) | `GET /files/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/filesList) |
| [List Groups](actions/list-groups.md) | `GET /groups/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Group/operation/groupsList) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/webhooksList) |
| [Store File](actions/store-file.md) | `PUT /files/:uuid/storage/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/storeFile) |
| [Update File Metadata Value](actions/update-file-metadata-value.md) | `PUT /files/:uuid/metadata/:key/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/updateFileMetadataKey) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id/` | [docs](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/updateWebhook) |
