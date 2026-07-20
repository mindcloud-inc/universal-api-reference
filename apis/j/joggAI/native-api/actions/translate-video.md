# Translate Video with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video_translate/`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Translate Video](https://docs.jogg.ai/api-reference/v2/Video/VideoTranslateCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `add_subtitles` | body | `boolean` | no | Whether to include subtitles |
| `callback_url` | body | `string` | no | Webhook callback URL for completion notifications |
| `enable_dynamic_duration` | body | `boolean` | no | Whether to adapt translated video duration dynamically |
| `output_language` | body | `string` | yes | Target language for translation |
| `output_voice` | body | `string` | no | Voice ID for dubbed audio |
| `title` | body | `string` | no | Title for the translated video |
| `translate_audio_only` | body | `boolean` | no | Translate audio only without lip sync |
| `video_url` | body | `string` | yes | URL of the video to translate |
