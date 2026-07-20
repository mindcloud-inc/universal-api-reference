# Get Video Task with ZapCap

Retrieves a video task from ZapCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:videoId/task/:id`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Get Video Task](https://platform.zapcap.ai/docs/api#tag/videos/get/videos/%7BvideoId%7D/task/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `id` | path | `string` | yes | ZapCap task ID. |
