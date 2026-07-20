# List Popular Videos with Pexels

Retrieves popular video results from Pexels.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/videos/popular`
- **Base URL:** `https://api.pexels.com`
- **Official documentation:** [List Popular Videos](https://www.pexels.com/api/documentation/#videos-popular)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min_width` | query | `number` | no | Minimum width in pixels of returned videos. |
| `min_height` | query | `number` | no | Minimum height in pixels of returned videos. |
| `min_duration` | query | `number` | no | Minimum duration in seconds of returned videos. |
| `max_duration` | query | `number` | no | Maximum duration in seconds of returned videos. |
