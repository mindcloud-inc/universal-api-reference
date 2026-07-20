# Add Subtitle To Video From File with Bookoly

Adds subtitles from a file to a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-subtitle-to-video-from-file`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Add Subtitle To Video From File](https://bookoly.com/docs/api/v1#/paths/~1add-subtitle-to-video-from-file/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `subtitle` | body | `object` | yes | — |
| `subtitle.type` | body | `list` | yes | Accepted values: `ass`. |
| `subtitle.url` | body | `string` | yes | — |
