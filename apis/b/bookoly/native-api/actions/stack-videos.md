# Stack Videos with Bookoly

Creates a stacked video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/stack-videos`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Stack Videos](https://bookoly.com/docs/api/v1#/paths/~1stack-videos/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `video.mute` | body | `boolean` | yes | — |
| `secondary_video` | body | `object` | yes | — |
| `secondary_video.url` | body | `string` | yes | — |
| `secondary_video.mute` | body | `boolean` | yes | — |
| `stack_option` | body | `object` | yes | — |
| `stack_option.layout` | body | `list` | yes | Accepted values: `horizontal`, `vertical`. |
