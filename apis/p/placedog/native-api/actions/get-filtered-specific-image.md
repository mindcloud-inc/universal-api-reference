# Get Filtered Specific Image with Placedog

Retrieves a filtered Placedog image by image ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:width]/[:height]/[:filter]`
- **Base URL:** `https://placedog.net`
- **Official documentation:** [Get Filtered Specific Image](https://placedog.net/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | path | `number` | yes | — |
| `height` | path | `number` | yes | — |
| `filter` | path | `list` | yes | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `id` | query | `number` | yes | — |
