# <img src="https://images.mindcloud.co/apps/icons/cloudinary_1773333349234.png" alt="Cloudinary logo" width="28" height="28"> Cloudinary: Universal API

Upload, manage, search, and transform media assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudinary/latest
- **Category:** Content & Files / Storage
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudinary.com
- **Vendor API docs:** https://cloudinary.com/documentation/cloudinary_references

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Apply Explicit Asset Actions](actions/apply-explicit-asset-actions.md) | PUT | Applies explicit asset actions in Cloudinary. |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an asset from your Cloudinary account. |
| [Rename Asset](actions/rename-asset.md) | PUT | Renames an asset in your Cloudinary account. |
| [Upload Asset](actions/upload-asset.md) | POST | Uploads an asset to your Cloudinary account. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in your Cloudinary account. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from your Cloudinary account. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from your Cloudinary account. |
| [List Subfolders](actions/list-subfolders.md) | GET | Retrieves subfolders from a Cloudinary folder. |
| [Search Folders](actions/search-folders.md) | GET | Finds folders in Cloudinary by search expression. |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Pings the Cloudinary Admin API connection. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Delete Resources by Asset IDs](actions/delete-resources-by-asset-ids.md) | DELETE | Deletes Cloudinary resources by asset IDs. |
| [Delete Resources by Public IDs](actions/delete-resources-by-public-ids.md) | DELETE | Deletes Cloudinary resources by public IDs. |
| [Get Resource by Asset ID](actions/get-resource-by-asset-id.md) | GET | Retrieves a Cloudinary resource by asset ID. |
| [Get Resource by Public ID](actions/get-resource-by-public-id.md) | GET | Retrieves a Cloudinary resource by public ID. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from your Cloudinary account. |
| [List Resources by Asset Folder](actions/list-resources-by-asset-folder.md) | GET | Retrieves resources from a specific Cloudinary asset folder. |
| [List Resources by Tag](actions/list-resources-by-tag.md) | GET | Retrieves Cloudinary resources by tag value. |
| [Search Resources](actions/search-resources.md) | GET | Finds resources in Cloudinary by search expression. |
| [Update Resource Details](actions/update-resource-details.md) | PUT | Updates resource details in your Cloudinary account. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from your Cloudinary account. |

### Upload Preset

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload Preset](actions/create-upload-preset.md) | POST | Creates an upload preset in Cloudinary. |
| [Delete Upload Preset](actions/delete-upload-preset.md) | DELETE | Deletes an upload preset from Cloudinary. |
| [Get Upload Preset](actions/get-upload-preset.md) | GET | Retrieves an upload preset from Cloudinary. |
| [List Upload Presets](actions/list-upload-presets.md) | GET | Retrieves upload presets from your Cloudinary account. |
| [Update Upload Preset](actions/update-upload-preset.md) | PUT | Updates an upload preset in Cloudinary. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves account usage details from Cloudinary. |

