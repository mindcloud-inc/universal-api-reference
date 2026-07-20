# List Channels with YouTube

Retrieves one or more channels from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/channels`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Channels](https://developers.google.com/youtube/v3/docs/channels/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated list of one or more channel resource properties. |
| `id` | query | `string` | no | Comma-separated YouTube channel IDs. Send multiple values as a string separated by `,`. |
| `mine` | query | `boolean` | no | Return channels owned by the authenticated user. |
