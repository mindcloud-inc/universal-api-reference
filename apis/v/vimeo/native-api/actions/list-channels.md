# List Channels with Vimeo

Retrieves channel records from the Vimeo API.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Channels](https://developer.vimeo.com/api/reference/channels#get_channels)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | The search query to use to filter the returned channels. |
| `filter` | query | `list` | no | Return only channels that match the selected channel filter. Accepted values: `featured`. |
