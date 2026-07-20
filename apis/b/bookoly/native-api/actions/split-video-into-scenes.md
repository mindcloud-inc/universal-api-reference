# Split Video Into Scenes with Bookoly

Splits a video into scenes in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/split-video-into-scenes`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Split Video Into Scenes](https://bookoly.com/docs/api/v1#/paths/~1split-video-into-scenes/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `video.mute` | body | `boolean` | yes | — |
| `split_option` | body | `object` | yes | — |
| `split_option.type` | body | `list` | yes | Accepted values: `auto`, `count`, `time`. |
