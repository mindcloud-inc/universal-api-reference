# ImageKit.io: Native API Reference

A consolidated summary of ImageKit.io's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://imagekit.io/docs/api-reference
- **API base URL:** `https://api.imagekit.io/v1`

## Authentication

### Basic Auth (Private API Key)

Use your ImageKit Private API Key as the Basic username; leave password empty.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://imagekit.io/docs/api-keys)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–1000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags Bulk](actions/add-tags-bulk.md) | `POST /files/addTags` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/add-tags-bulk) |
| [Bulk Job Status](actions/bulk-job-status.md) | `GET /bulkJobs/:jobId` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/bulk-job-status) |
| [Copy Folder](actions/copy-folder.md) | `POST /bulkJobs/copyFolder` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/copy-folder) |
| [Create Extension](actions/create-extension.md) | `POST /saved-extensions` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/saved-extensions/create-extension) |
| [Create Folder](actions/create-folder.md) | `POST /folder` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/create-folder) |
| [Create New Field](actions/create-new-field.md) | `POST /customMetadataFields` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/custom-metadata-fields/create-new-field) |
| [Delete File Version](actions/delete-file-version.md) | `DELETE /files/:fileId/versions/:versionId` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/delete-file-version) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folder` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/delete-folder) |
| [Delete Multiple Files](actions/delete-multiple-files.md) | `POST /files/batch/deleteByFileIds` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/delete-multiple-files) |
| [Get Extension](actions/get-extension.md) | `GET /saved-extensions/:extensionId` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/saved-extensions/get-extension) |
| [Get File Details](actions/get-file-details.md) | `GET /files/:fileId/details` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/get-file-details) |
| [Get File Version Details](actions/get-file-version-details.md) | `GET /files/:fileId/versions/:versionId` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/get-file-version-details) |
| [Get Metadata From URL](actions/get-metadata-from-url.md) | `GET /metadata` | [docs](https://imagekit.io/docs/api-reference/file-metadata/get-metadata-from-url) |
| [Get Uploaded File Metadata](actions/get-uploaded-file-metadata.md) | `GET /files/:fileId/metadata` | [docs](https://imagekit.io/docs/api-reference/file-metadata/get-uploaded-file-metadata) |
| [Get Usage](actions/get-usage.md) | `GET /accounts/usage` | [docs](https://imagekit.io/docs/api-reference/account-management-api/get-usage) |
| [List All Fields](actions/list-all-fields.md) | `GET /customMetadataFields` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/custom-metadata-fields/list-all-fields) |
| [List and Search Assets](actions/list-and-search-assets.md) | `GET /files` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/list-and-search-assets) |
| [List Extensions](actions/list-extensions.md) | `GET /saved-extensions` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/saved-extensions/list-extensions) |
| [List File Versions](actions/list-file-versions.md) | `GET /files/:fileId/versions` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/list-file-versions) |
| [Move Folder](actions/move-folder.md) | `POST /bulkJobs/moveFolder` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/move-folder) |
| [Purge Cache](actions/purge-cache.md) | `POST /files/purge` | [docs](https://imagekit.io/docs/api-reference/caching/purge-cache) |
| [Purge Status](actions/purge-status.md) | `GET /files/purge/:requestId` | [docs](https://imagekit.io/docs/api-reference/caching/purge-status) |
| [Remove AI Tags Bulk](actions/remove-ai-tags-bulk.md) | `POST /files/removeAITags` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/remove-ai-tags-bulk) |
| [Remove Tags Bulk](actions/remove-tags-bulk.md) | `POST /files/removeTags` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/remove-tags-bulk) |
| [Rename File](actions/rename-file.md) | `PUT /files/rename` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/rename-file) |
| [Rename Folder](actions/rename-folder.md) | `POST /bulkJobs/renameFolder` | [docs](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/rename-folder) |
| [Upload File](actions/upload-file.md) | `POST https://upload.imagekit.io/api/v1/files/upload` | [docs](https://imagekit.io/docs/api-reference/upload-file/upload-file) |
| [Upload File V2](actions/upload-file-v2.md) | `POST https://upload.imagekit.io/api/v2/files/upload` | [docs](https://imagekit.io/docs/api-reference/upload-file/upload-file-v2) |
