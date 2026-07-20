# Create Task With Export Settings with ZapCap

Creates a caption task in ZapCap with export settings.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/task`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Create Task With Export Settings](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `templateId` | body | `string` | yes | ZapCap template ID. |
| `autoApprove` | body | `boolean` | yes | Automatically approve the transcript. |
| `exportSettings` | body | `object` | yes | ZapCap export settings object. |
