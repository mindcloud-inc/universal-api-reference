# Screenly: Native API Reference

A consolidated summary of Screenly's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://developer.screenly.io/api/
- **API base URL:** `https://api.screenlyapp.com/api/v3`

## Authentication

### API Token

Authenticate Screenly requests with a Screenly API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.screenly.io/hc/en-us/articles/35897560148371-How-to-Generate-a-Screenly-API-Token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | `POST /assets/` | [docs](https://developer.screenly.io/api/#assets_create) |
| [Create Group](actions/create-group.md) | `POST /groups/` | [docs](https://developer.screenly.io/api/#groups_create) |
| [Create Playlist](actions/create-playlist.md) | `POST /playlists/` | [docs](https://developer.screenly.io/api/#playlists_create) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /assets/:id/` | [docs](https://developer.screenly.io/api/#assets_delete) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id/` | [docs](https://developer.screenly.io/api/#groups_delete) |
| [Delete Playlist](actions/delete-playlist.md) | `DELETE /playlists/:id/` | [docs](https://developer.screenly.io/api/#playlists_delete) |
| [Get Asset](actions/get-asset.md) | `GET /assets/:id/` | [docs](https://developer.screenly.io/api/#assets_read) |
| [Get Group](actions/get-group.md) | `GET /groups/:id/` | [docs](https://developer.screenly.io/api/#groups_read) |
| [Get Playlist](actions/get-playlist.md) | `GET /playlists/:id/` | [docs](https://developer.screenly.io/api/#playlists_read) |
| [List Assets](actions/list-assets.md) | `GET /assets/` | [docs](https://developer.screenly.io/api/#assets_list) |
| [List Groups](actions/list-groups.md) | `GET /groups/` | [docs](https://developer.screenly.io/api/#groups_list) |
| [List Playlists](actions/list-playlists.md) | `GET /playlists/` | [docs](https://developer.screenly.io/api/#playlists_list) |
| [List Screens](actions/list-screens.md) | `GET /screens/` | [docs](https://developer.screenly.io/api/#screens_list) |
| [Update Asset](actions/update-asset.md) | `PATCH /assets/:id/` | [docs](https://developer.screenly.io/api/#assets_partial_update) |
| [Update Group](actions/update-group.md) | `PATCH /groups/:id/` | [docs](https://developer.screenly.io/api/#groups_partial_update) |
| [Update Playlist](actions/update-playlist.md) | `PATCH /playlists/:id/` | [docs](https://developer.screenly.io/api/#playlists_partial_update) |
