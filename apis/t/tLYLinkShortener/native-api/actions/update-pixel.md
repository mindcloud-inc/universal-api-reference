# Update Pixel with TLY Link Shortener

Updates an existing pixel in TLY Link Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/link/pixel/:id`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Update Pixel](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The pixel ID to update. |
| `name` | body | `string` | no | The updated pixel display name. |
| `pixel_id` | body | `string` | no | The updated provider pixel identifier. |
| `pixel_type` | body | `string` | no | The updated pixel provider type. |
