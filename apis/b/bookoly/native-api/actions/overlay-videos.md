# Overlay Videos with Bookoly

Creates an overlay video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/overlay-videos`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Overlay Videos](https://bookoly.com/docs/api/v1#/paths/~1overlay-videos/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `video.mute` | body | `boolean` | yes | — |
| `overlay_video` | body | `object` | yes | — |
| `overlay_video.url` | body | `string` | yes | — |
| `overlay_video.mute` | body | `boolean` | yes | — |
| `overlay_option` | body | `object` | yes | — |
| `overlay_option.position` | body | `list` | yes | Accepted values: `bottom_left`, `bottom_right`, `center`, `center_bottom`, `center_left`, `center_right`, `center_top`, `top_left`, `top_right`. |
