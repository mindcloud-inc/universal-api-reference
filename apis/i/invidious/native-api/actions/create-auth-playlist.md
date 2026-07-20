# Create Auth Playlist with Invidious

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/playlists`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Create Auth Playlist](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `privacy` | body | `string` | no | Playlist privacy: public, unlisted, or private. |
| `title` | body | `string` | yes | Playlist title. |
