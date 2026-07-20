# Mute Video with Bookoly

Removes audio from a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/mute-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Mute Video](https://bookoly.com/docs/api/v1#/paths/~1mute-a-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
