# Get Filtered Placeholder Image with Placedog

Retrieves a filtered placeholder dog image from Placedog.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:width]/[:height]/[:filter]`
- **Base URL:** `https://placedog.net`
- **Official documentation:** [Get Filtered Placeholder Image](https://placedog.net/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | path | `number` | yes | — |
| `height` | path | `number` | yes | — |
| `filter` | path | `list` | yes | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
