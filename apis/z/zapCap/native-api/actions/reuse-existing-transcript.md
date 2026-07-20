# Reuse Existing Transcript with ZapCap

Creates a caption task in ZapCap from an existing transcript.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/task`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Reuse Existing Transcript](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID. |
| `templateId` | body | `string` | yes | ZapCap template ID. |
| `autoApprove` | body | `boolean` | yes | Automatically approve the transcript. |
| `transcriptTaskId` | body | `string` | yes | Existing successful ZapCap transcript task ID to reuse. |
