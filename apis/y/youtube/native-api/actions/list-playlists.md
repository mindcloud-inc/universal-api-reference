# List Playlists with YouTube

Retrieves one or more playlists from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/playlists`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Playlists](https://developers.google.com/youtube/v3/docs/playlists/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Response parts to include. |
| `channelId` | query | `string` | no | Return playlists for a channel. |
| `id` | query | `string` | no | Comma-separated playlist IDs. Send multiple values as a string separated by `,`. |
| `mine` | query | `boolean` | no | Return playlists owned by the authenticated YouTube channel. |
