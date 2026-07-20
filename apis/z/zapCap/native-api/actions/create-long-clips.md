# Create Long Clips with ZapCap

Creates a long clip task in ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/clipTask`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Create Long Clips](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/clipTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `maxClips` | body | `number` | yes | Maximum number of clips to generate. |
| `durationRange` | body | `string` | yes | Desired clip duration range enum. |
