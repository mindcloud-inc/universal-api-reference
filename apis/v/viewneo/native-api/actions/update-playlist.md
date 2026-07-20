# Update Playlist with Viewneo

Updates an existing playlist in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/playlist/:id`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Update Playlist](https://cloud.viewneo.com/doc/api#/Playlist/api.playlist.update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
