# List Playlist Items with YouTube

Retrieves items from a YouTube playlist.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/playlistItems`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Playlist Items](https://developers.google.com/youtube/v3/docs/playlistItems/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Response parts to include. |
| `playlistId` | query | `string` | no | The playlist ID to list items for. |
| `id` | query | `string` | no | Comma-separated playlist item IDs. Send multiple values as a string separated by `,`. |
