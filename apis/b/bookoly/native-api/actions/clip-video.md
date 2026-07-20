# Clip Video with Bookoly

Clips a video to a selected segment in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/clip-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Clip Video](https://bookoly.com/docs/api/v1#/paths/~1clip-a-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
| `video.mute` | body | `boolean` | yes |
| `clip_option` | body | `object` | yes |
| `clip_option.start` | body | `number` | yes |
