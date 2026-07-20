# Create Library Asset with Storyscale

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/library/create`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Create Library Asset](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_description` | body | `string` | no | Description of the library asset. |
| `asset_friendly_name` | body | `string` | no | User-facing name for the library asset. |
| `asset_type_id` | body | `number` | no | The asset type for the new library asset. |
| `asset_url` | body | `string` | no | Source URL for the library asset. |
| `cover_image_url` | body | `string` | no | Cover image URL for the library asset. |
| `reading_time` | body | `number` | no | Estimated reading time for the asset. |
