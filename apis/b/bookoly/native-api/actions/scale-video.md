# Scale Video with Bookoly

Scales a video to new dimensions in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/scale-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Scale Video](https://bookoly.com/docs/api/v1#/paths/~1scale-a-video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `video.mute` | body | `boolean` | yes | — |
| `scale_option` | body | `object` | yes | — |
| `scale_option.mode` | body | `list` | yes | Accepted values: `scale_exact`, `scale_keep_aspect_ratio`, `scale_to_fill`, `scale_to_fit`, `scale_to_height`, `scale_to_width`. |
