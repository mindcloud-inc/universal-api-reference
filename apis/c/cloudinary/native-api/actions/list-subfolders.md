# List Subfolders with Cloudinary

Retrieves subfolders from a Cloudinary folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [List Subfolders](https://cloudinary.com/documentation/admin_api#folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | path | `string` | yes | The folder path to retrieve. |
