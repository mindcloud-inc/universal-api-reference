# Add Video To Auth Playlist with Invidious

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/playlists/:id/videos`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Add Video To Auth Playlist](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Authenticated playlist ID. |
| `videoId` | body | `string` | yes | Video ID to add to the playlist. |
