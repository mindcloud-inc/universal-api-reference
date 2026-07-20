# List Channel Videos with Vimeo

Retrieves videos in a Vimeo channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channel_id/videos`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Channel Videos](https://developer.vimeo.com/api/reference/channels#get_channel_videos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `number` | yes | The ID of the channel. |
| `containing_uri` | query | `string` | no | The page that contains the video URI. |
| `filter` | query | `list` | no | The attribute by which to filter the results. Accepted values: `embeddable`. |
| `filter_embeddable` | query | `boolean` | no | Whether to filter the results by embeddable or non-embeddable videos. |
| `query` | query | `string` | no | The search query to use to filter the results. |
| `sizes` | query | `string` | no | The pixel dimensions of the image in {width}x{height} format. |
