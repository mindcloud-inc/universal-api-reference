# Extract Audio From Video with Bookoly

Extracts audio from a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract-audio-from-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Extract Audio From Video](https://bookoly.com/docs/api/v1#/paths/~1extract-audio-from-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
