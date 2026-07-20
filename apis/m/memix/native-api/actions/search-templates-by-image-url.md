# Search Templates By Image URL with Memix

Finds templates in Memix by image URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates/search`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | query | `string` | yes | Image URL used to discover matching templates. |
| `limit` | query | `number` | no | Maximum number of templates to return. |
