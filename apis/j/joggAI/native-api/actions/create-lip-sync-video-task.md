# Create Lip Sync Video Task with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create_lip_sync_video`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Lip Sync Video Task](https://docs.jogg.ai/api-reference/v2/Video/CreateLipSyncVideo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Source audio URL |
| `playback_type` | body | `string` | no | Playback strategy when the source video is shorter than the audio |
| `video_url` | body | `string` | yes | Source video URL |
