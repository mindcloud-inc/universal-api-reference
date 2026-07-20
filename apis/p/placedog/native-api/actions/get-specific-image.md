# Get Specific Image with Placedog

Retrieves a specific Placedog image by image ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:width]/[:height]`
- **Base URL:** `https://placedog.net`
- **Official documentation:** [Get Specific Image](https://placedog.net/images)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `width` | path | `number` | yes |
| `height` | path | `number` | yes |
| `id` | query | `number` | yes |
