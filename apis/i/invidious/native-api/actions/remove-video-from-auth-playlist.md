# Remove Video From Auth Playlist with Invidious

## Endpoint

- **Method:** `DELETE`
- **Path:** `/auth/playlists/:id/videos/:index`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Remove Video From Auth Playlist](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Authenticated playlist ID. |
| `index` | path | `string` | yes | Playlist video indexId to remove. |
