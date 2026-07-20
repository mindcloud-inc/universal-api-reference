# Generate Lip Sync Video with Pipio

Creates a lip-synced video in Pipio from source video and audio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://project.pipio.ai/project/generate/lipsync`
- **Base URL:** `https://avatar.pipio.ai`
- **Official documentation:** [Generate Lip Sync Video](https://docs.pipio.ai/lip-sync-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceUrl` | body | `string` | yes | The URL to your source video that will be lip-synced. |
| `targetAudioUrl` | body | `string` | yes | The URL to the audio file that will be synced to the video. |
