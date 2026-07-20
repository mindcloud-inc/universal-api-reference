# Update Auth Playlist with Invidious

## Endpoint

- **Method:** `PATCH`
- **Path:** `/auth/playlists/:id`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Update Auth Playlist](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | New playlist description. |
| `id` | path | `string` | yes | Authenticated playlist ID. |
| `privacy` | body | `string` | no | Playlist privacy: public, unlisted, or private. |
| `title` | body | `string` | no | New playlist title. |
