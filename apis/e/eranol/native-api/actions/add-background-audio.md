# Add Background Audio with Eranol

Creates a background audio job in Eranol.

## Endpoint

- **Method:** `POST`
- **Path:** `/ffmpeg/video/add-bg-audio`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Add Background Audio](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_url` | body | `string` | yes | Source video URL |
| `bg_audio_url` | body | `string` | yes | Background audio file URL |
| `bg_audio_volume` | body | `number` | no | Background audio mix volume |
