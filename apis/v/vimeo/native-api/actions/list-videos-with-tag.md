# List Videos with Tag with Vimeo

Retrieves videos with a specific tag from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/:word/videos`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Videos with Tag](https://developer.vimeo.com/api/reference/videos#get_videos_with_tag)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `word` | path | `string` | yes | The tag word. |
