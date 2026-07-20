# List all video objects with api.video

Retrieves all video objects from api.video.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [List all video objects](https://docs.api.video/reference/api/Videos#list-all-video-objects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currentPage` | query | `number` | no | Optional page number for the video list request. |
| `pageSize` | query | `number` | no | Optional page size for the video list request. |
| `title` | query | `string` | no | Optional title filter for the video list request. |
