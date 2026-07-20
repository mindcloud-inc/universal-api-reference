# <img src="https://images.mindcloud.co/apps/icons/image-kit_1771619894158.png" alt="ImageKit.io logo" width="28" height="28"> ImageKit.io: Universal API

Optimize media, transform assets, manage libraries, and deliver visuals fast.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imageKit/latest
- **Category:** Content & Files / Storage
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://imagekit.io
- **Vendor API docs:** https://imagekit.io/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List and Search Assets](actions/list-and-search-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-and-search-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Cache

| Action | Method | Description |
| --- | --- | --- |
| [Purge Cache](actions/purge-cache.md) | PUT | Purges cached file URLs in ImageKit.io. |
| [Purge Status](actions/purge-status.md) | GET | Retrieves the status of a cache purge request in ImageKit.io. |

### Custom Metadata Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create New Field](actions/create-new-field.md) | POST | Creates a custom metadata field in ImageKit.io. |
| [List All Fields](actions/list-all-fields.md) | GET | Retrieves custom metadata fields from ImageKit.io. |

### Extensions

| Action | Method | Description |
| --- | --- | --- |
| [Create Extension](actions/create-extension.md) | POST | Creates a saved extension in ImageKit.io. |
| [Get Extension](actions/get-extension.md) | GET | Retrieves a saved extension from ImageKit.io. |
| [List Extensions](actions/list-extensions.md) | GET | Retrieves saved extensions from your ImageKit.io account. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List and Search Assets](actions/list-and-search-assets.md) | GET | Finds files in ImageKit.io with search and filter options. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags Bulk](actions/add-tags-bulk.md) | PUT | Adds tags to multiple files in ImageKit.io. |
| [Delete File Version](actions/delete-file-version.md) | DELETE | Deletes a file version from ImageKit.io. |
| [Delete Multiple Files](actions/delete-multiple-files.md) | DELETE | Deletes multiple files from the ImageKit.io media library. |
| [Get File Details](actions/get-file-details.md) | GET | Retrieves detailed file information from ImageKit.io. |
| [Get File Version Details](actions/get-file-version-details.md) | GET | Retrieves file version details from ImageKit.io. |
| [List File Versions](actions/list-file-versions.md) | GET | Retrieves all file versions from ImageKit.io. |
| [Remove AI Tags Bulk](actions/remove-ai-tags-bulk.md) | PUT | Removes AI tags from multiple files in ImageKit.io. |
| [Remove Tags Bulk](actions/remove-tags-bulk.md) | PUT | Removes tags from multiple files in ImageKit.io. |
| [Rename File](actions/rename-file.md) | PUT | Renames an existing file in ImageKit.io. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to your ImageKit.io account. |
| [Upload File V2](actions/upload-file-v2.md) | POST | Uploads a file to ImageKit.io using Upload API v2. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Job Status](actions/bulk-job-status.md) | GET | Retrieves the status of a folder bulk job in ImageKit.io. |
| [Copy Folder](actions/copy-folder.md) | PUT | Starts a folder copy job in ImageKit.io. |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in ImageKit.io. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from ImageKit.io. |
| [Move Folder](actions/move-folder.md) | PUT | Starts a folder move job in ImageKit.io. |
| [Rename Folder](actions/rename-folder.md) | PUT | Starts a folder rename job in ImageKit.io. |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Metadata From URL](actions/get-metadata-from-url.md) | GET | Retrieves file metadata from a URL in ImageKit.io. |
| [Get Uploaded File Metadata](actions/get-uploaded-file-metadata.md) | GET | Retrieves uploaded file metadata from ImageKit.io. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves account usage metrics from ImageKit.io. |

