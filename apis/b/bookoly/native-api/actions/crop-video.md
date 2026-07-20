# Crop Video with Bookoly

Crops a video to a selected area in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/crop-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Crop Video](https://bookoly.com/docs/api/v1#/paths/~1crop-a-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
| `video.mute` | body | `boolean` | yes |
| `crop_option` | body | `object` | yes |
| `crop_option.point` | body | `object` | yes |
| `crop_option.point.x` | body | `number` | yes |
| `crop_option.point.y` | body | `number` | yes |
| `crop_option.width` | body | `number` | yes |
| `crop_option.height` | body | `number` | yes |
