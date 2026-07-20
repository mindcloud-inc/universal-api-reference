# Create Green Screen Export with ZapCap

Creates a green screen export task in ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/task`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Create Green Screen Export](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `templateId` | body | `string` | yes | ZapCap template ID. |
| `autoApprove` | body | `boolean` | yes | Automatically approve the transcript. |
| `exportSettings.greenScreen` | body | `boolean` | yes | Enable green screen export. |
