# Create Translated Subtitle Task with ZapCap

Creates a translated subtitle task in ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/task`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Create Translated Subtitle Task](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `templateId` | body | `string` | yes | ZapCap template ID. |
| `autoApprove` | body | `boolean` | yes | Automatically approve the transcript. |
| `translateTo` | body | `string` | yes | Target subtitle language code. |
