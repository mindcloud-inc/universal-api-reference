# Approve Transcript with ZapCap

Approves a transcript for a ZapCap task.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/task/:id/approve-transcript`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Approve Transcript](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task/%7Bid%7D/approve-transcript)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | path | `string` | yes | ZapCap video ID that owns the task. |
| `id` | path | `string` | yes | Caption task ID to approve. |
