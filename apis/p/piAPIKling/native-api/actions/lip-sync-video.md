# Lip Sync Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Lip Sync Video](https://piapi.ai/docs/kling-api/lipsync-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.origin_task_id` | body | `string` | no | Existing Kling task ID to lip-sync. Use this or Video URL. |
| `input.video_url` | body | `string` | no | External video URL to lip-sync. Use this or Origin Task ID. |
| `input.tts_text` | body | `string` | no | Text for Kling to synthesize before lip-syncing. Use this or Dubbing Audio URL. |
| `input.tts_timbre` | body | `string` | no | Kling TTS voice or timbre name. |
| `input.tts_speed` | body | `number` | no | Speech speed multiplier for Kling TTS. |
| `input.local_dubbing_url` | body | `string` | no | Existing audio URL to lip-sync. Use this or TTS Text. |
