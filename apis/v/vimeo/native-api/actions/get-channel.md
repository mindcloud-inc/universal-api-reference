# Get Channel with Vimeo

Retrieves a channel record from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channel_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Get Channel](https://developer.vimeo.com/api/reference/channels#get_channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `number` | yes | The ID of the channel. |
| `sizes` | query | `string` | no | The pixel dimensions of the image in {width}x{height} format. |
