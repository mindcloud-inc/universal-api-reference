# Add Watermark To Video with Bookoly

Adds a watermark to a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-watermark-to-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Add Watermark To Video](https://bookoly.com/docs/api/v1#/paths/~1add-watermark-to-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
| `video.mute` | body | `boolean` | yes |
| `watermark` | body | `object` | yes |
| `watermark.point` | body | `object` | yes |
| `watermark.point.x` | body | `number` | yes |
| `watermark.point.y` | body | `number` | yes |
| `watermark.url` | body | `string` | yes |
