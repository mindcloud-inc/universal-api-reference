# Update Playlist with YouTube

Updates an existing playlist in YouTube.

## Endpoint

- **Method:** `PUT`
- **Path:** `/youtube/v3/playlists`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Update Playlist](https://developers.google.com/youtube/v3/docs/playlists/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated playlist resource parts to include in the response and update. |
| `id` | body | `string` | yes | Playlist ID. |
| `snippet.title` | body | `string` | yes | Playlist title. |
| `snippet.description` | body | `string` | no | Playlist description. |
| `status.privacyStatus` | body | `string` | no | Playlist visibility status. |
| `onBehalfOfContentOwner` | query | `string` | no | Content owner ID when acting on behalf of a CMS user. |
