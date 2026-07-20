# Delete Resources by Asset IDs with Cloudinary

Deletes Cloudinary resources by asset IDs.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/resources`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Delete Resources by Asset IDs](https://cloudinary.com/documentation/admin_api#delete_resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_ids[]` | body | `array<string>` | yes | The asset IDs to delete. |
