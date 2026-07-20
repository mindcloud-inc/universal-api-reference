# Frame Video with Bookoly

Creates a video frame image in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/frame-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Frame Video](https://bookoly.com/docs/api/v1#/paths/~1frame-a-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
| `frame` | body | `object` | yes |
| `frame.seconds` | body | `number` | yes |
