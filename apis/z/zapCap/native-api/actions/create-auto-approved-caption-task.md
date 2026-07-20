# Create Auto-Approved Caption Task with ZapCap

Creates an auto-approved caption task in ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/task`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Create Auto-Approved Caption Task](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID to process. |
| `templateId` | body | `string` | yes | Caption template ID from List Templates. |
| `language` | body | `string` | no | Language code for transcription. |
