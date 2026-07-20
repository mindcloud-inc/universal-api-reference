# Get Viral Clip Task Status with ZapCap

Retrieves clip task status from ZapCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:videoId/clipTask/:id`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Get Viral Clip Task Status](https://platform.zapcap.ai/docs/api#tag/videos/get/videos/%7BvideoId%7D/clipTask/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `id` | path | `string` | yes | ZapCap clip task ID. |
