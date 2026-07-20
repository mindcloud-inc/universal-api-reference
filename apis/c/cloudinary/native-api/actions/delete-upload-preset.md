# Delete Upload Preset with Cloudinary

Deletes an upload preset from Cloudinary.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/upload_presets/:name`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Delete Upload Preset](https://cloudinary.com/documentation/admin_api#delete_an_upload_preset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The upload preset name to delete. |
