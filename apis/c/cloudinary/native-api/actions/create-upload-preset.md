# Create Upload Preset with Cloudinary

Creates an upload preset in Cloudinary.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload_presets`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Create Upload Preset](https://cloudinary.com/documentation/admin_api#upload_presets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The upload preset name to create. |
| `unsigned` | body | `boolean` | no | Whether the preset allows unsigned uploads. |
