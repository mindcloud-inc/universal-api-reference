# Blur Video with Bookoly

Blurs a selected area of a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/blur-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Blur Video](https://bookoly.com/docs/api/v1#/paths/~1blur-a-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
| `video.mute` | body | `boolean` | yes |
| `blur_option` | body | `object` | yes |
| `blur_option.point` | body | `object` | yes |
| `blur_option.point.x` | body | `number` | yes |
| `blur_option.point.y` | body | `number` | yes |
| `box_width` | body | `number` | yes |
| `box_height` | body | `number` | yes |
| `blur_option.power` | body | `number` | yes |
