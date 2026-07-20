# Update Playlist with Screenly

Updates an existing playlist in Screenly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/playlists/:id/`
- **Base URL:** `https://api.screenlyapp.com/api/v3`
- **Official documentation:** [Update Playlist](https://developer.screenly.io/api/#playlists_partial_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `is_enabled` | body | `boolean` | no |
| `predicate` | body | `string` | no |
| `priority` | body | `number` | no |
| `title` | body | `string` | no |
