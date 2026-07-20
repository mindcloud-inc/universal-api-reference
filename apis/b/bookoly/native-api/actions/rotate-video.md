# Rotate Video with Bookoly

Rotates a video by fixed degrees in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/rotate-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Rotate Video](https://bookoly.com/docs/api/v1#/paths/~1rotate-a-video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `video.mute` | body | `boolean` | yes | — |
| `rotation_degrees` | body | `list` | yes | Accepted values: `180`, `270`, `90`. |
