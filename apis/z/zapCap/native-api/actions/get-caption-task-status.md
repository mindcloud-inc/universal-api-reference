# Get Caption Task Status with ZapCap

Retrieves caption task status from ZapCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:videoId/task/:id`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Get Caption Task Status](https://platform.zapcap.ai/docs/api#tag/videos/get/videos/%7BvideoId%7D/task/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID that owns the task. |
| `id` | path | `string` | yes | Caption task ID to inspect. |
