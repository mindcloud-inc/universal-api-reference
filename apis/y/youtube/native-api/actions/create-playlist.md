# Create Playlist with YouTube

Creates a new playlist in YouTube.

## Endpoint

- **Method:** `POST`
- **Path:** `/youtube/v3/playlists`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Create Playlist](https://developers.google.com/youtube/v3/docs/playlists/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated playlist resource parts to include in the response and update. |
| `snippet.title` | body | `string` | yes | Playlist title. |
| `snippet.description` | body | `string` | no | Playlist description. |
| `status.privacyStatus` | body | `string` | no | Playlist visibility status. |
| `snippet.tags[]` | body | `array<string>` | no | Playlist tags. |
| `onBehalfOfContentOwner` | query | `string` | no | Content owner ID when acting on behalf of a CMS user. |
