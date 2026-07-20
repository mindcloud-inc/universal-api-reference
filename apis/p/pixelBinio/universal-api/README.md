# <img src="https://images.mindcloud.co/apps/icons/pixel-binio_1775669005238.png" alt="PixelBin.io logo" width="28" height="28"> PixelBin.io: Universal API

PixelBin.io is a media storage and transformation platform for uploading, organizing, searching, transforming, and delivering assets through its platform APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pixelBinio/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pixelbin.io
- **Vendor API docs:** https://www.pixelbin.io/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get App Org Details](actions/get-app-org-details.md) | GET | Retrieves app and organization details from PixelBin.io. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from PixelBin.io. |
| [Delete Files](actions/delete-files.md) | DELETE | Deletes multiple files from PixelBin.io storage. |
| [Upload File](actions/file-upload.md) | POST | Creates a new uploaded file in PixelBin.io. |
| [Get File By File ID](actions/get-file-by-file-id.md) | GET | Retrieves a file from PixelBin.io by file ID. |
| [Get File By ID](actions/get-file-by-id.md) | GET | Retrieves a file from PixelBin.io by internal ID. |
| [List Files](actions/list-files.md) | GET | Retrieves files and folders from PixelBin.io storage. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in PixelBin.io. |
| [Upload Asset From URL](actions/url-upload.md) | POST | Creates a new uploaded file in PixelBin.io from a URL. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in PixelBin.io. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from PixelBin.io. |
| [Get Folder Ancestors](actions/get-folder-ancestors.md) | GET | Retrieves folder ancestors from PixelBin.io storage. |
| [Get Folder Details](actions/get-folder-details.md) | GET | Retrieves folder details from PixelBin.io storage. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in PixelBin.io. |

### Playground Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Asset For Playground](actions/get-default-asset-for-playground.md) | GET | Retrieves the default playground asset from PixelBin.io. |

### Preset

| Action | Method | Description |
| --- | --- | --- |
| [Add Preset](actions/add-preset.md) | POST | Creates a new preset in PixelBin.io. |
| [Delete Preset](actions/delete-preset.md) | DELETE | Deletes an existing preset from PixelBin.io. |
| [Get Preset](actions/get-preset.md) | GET | Retrieves a preset from PixelBin.io by name. |
| [List Presets](actions/list-presets.md) | GET | Retrieves preset records from your PixelBin.io account. |
| [Update Preset](actions/update-preset.md) | PUT | Updates an existing preset in PixelBin.io. |

### Signed Multipart Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Signed URL V2](actions/create-signed-url-v2.md) | POST | Creates a new signed multipart upload URL in PixelBin.io. |

### Signed Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Signed URL](actions/create-signed-url.md) | POST | Creates a new signed upload URL in PixelBin.io. |

### Subscription Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Usage](actions/get-subscription-usage.md) | GET | Retrieves subscription usage details from PixelBin.io. |

### Transformation Context

| Action | Method | Description |
| --- | --- | --- |
| [Get Transformation Context](actions/get-transformation-context.md) | GET | Retrieves transformation context from a PixelBin.io URL. |

### Transformation Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Transformation Module](actions/get-transformation-module.md) | GET | Retrieves a transformation module from PixelBin.io playground. |
| [List Transformation Modules](actions/list-transformation-modules.md) | GET | Retrieves transformation modules from the PixelBin.io playground. |

### Transformation Module Credentials

| Action | Method | Description |
| --- | --- | --- |
| [Add Transformation Module Credentials](actions/add-credentials.md) | POST | Creates new transformation module credentials in PixelBin.io. |
| [Delete Transformation Module Credentials](actions/delete-credentials.md) | DELETE | Deletes transformation module credentials from PixelBin.io. |
| [Update Transformation Module Credentials](actions/update-credentials.md) | PUT | Updates transformation module credentials in PixelBin.io. |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Usage](actions/get-current-usage.md) | GET | Retrieves current usage details from PixelBin.io. |

