# Create Asset with Voog

Creates a new asset in the current Voog site.

## Endpoint

- **Method:** `POST`
- **Path:** `/assets`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Asset](https://www.voog.com/developers/api/resources/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Filename for the asset to create. |
| `size` | body | `number` | yes | File size in bytes. |
| `content_type` | body | `string` | yes | MIME type of the asset file. |
| `width` | body | `number` | no | Image width in pixels when available. |
| `height` | body | `number` | no | Image height in pixels when available. |
