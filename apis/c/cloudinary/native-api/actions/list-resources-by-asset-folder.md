# List Resources by Asset Folder with Cloudinary

Retrieves resources from a specific Cloudinary asset folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/by_asset_folder`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [List Resources by Asset Folder](https://cloudinary.com/documentation/admin_api#resources_by_asset_folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_folder` | query | `string` | yes | The asset folder to list. |
