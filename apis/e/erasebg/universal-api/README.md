# <img src="https://images.mindcloud.co/apps/icons/erasebg_1775150488463.png" alt="Erase.bg logo" width="28" height="28"> Erase.bg: Universal API

Remove image backgrounds and manage AI media-processing assets with Erase.bg

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/erasebg/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.erase.bg/
- **Vendor API docs:** https://www.erase.bg/g/api/remove-background

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### App Details

| Action | Method | Description |
| --- | --- | --- |
| [Get App Details](actions/get-app-details.md) | GET | Retrieves app details from Erase.bg. |

### Default Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Asset For Playground](actions/get-default-asset-for-playground.md) | GET | Retrieves the default playground asset from Erase.bg. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Erase.bg storage. |
| [Get File By File ID](actions/get-file-by-file-id.md) | GET | Retrieves a file from Erase.bg by file ID. |
| [Get File By ID](actions/get-file-by-id.md) | GET | Retrieves a file from Erase.bg by internal ID. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Erase.bg storage by search filters. |
| [Update File](actions/update-file.md) | PUT | Updates a file in Erase.bg storage. |
| [Upload Asset From URL](actions/upload-asset-from-url.md) | POST | Creates a file in Erase.bg from a URL. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Files](actions/delete-files.md) | DELETE | Deletes multiple files from Erase.bg storage. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in Erase.bg storage. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from Erase.bg storage. |
| [Get Folder Details](actions/get-folder-details.md) | GET | Retrieves folder details from Erase.bg storage. |
| [Update Folder](actions/update-folder.md) | PUT | Updates a folder in Erase.bg storage. |

### Folder Ancestors

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder Ancestors](actions/get-folder-ancestors.md) | GET | Retrieves folder ancestors from Erase.bg storage. |

### Signed Multipart Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Signed Multipart Upload URL](actions/create-signed-multipart-upload-url.md) | POST | Creates a signed multipart upload URL in Erase.bg. |

### Signed Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Signed Upload URL](actions/create-signed-upload-url.md) | POST | Creates a signed upload URL in Erase.bg. |

### Transformation Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Transformation Module](actions/get-transformation-module.md) | GET | Retrieves a transformation module from Erase.bg. |

### Transformation Modules

| Action | Method | Description |
| --- | --- | --- |
| [Get Transformation Modules](actions/get-transformation-modules.md) | GET | Retrieves transformation modules from Erase.bg. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Usage](actions/get-current-usage.md) | GET | Retrieves current usage details from Erase.bg. |

