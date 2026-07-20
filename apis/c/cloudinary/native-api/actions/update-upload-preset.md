# Update Upload Preset with Cloudinary

Updates an upload preset in Cloudinary.

## Endpoint

- **Method:** `PUT`
- **Path:** `/upload_presets/:name`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Update Upload Preset](https://cloudinary.com/documentation/admin_api#upload_presets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The upload preset name to update. |
| `unsigned` | body | `boolean` | no | Whether the preset allows unsigned uploads. |
