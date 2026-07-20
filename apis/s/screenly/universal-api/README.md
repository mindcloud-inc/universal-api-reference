# <img src="https://images.mindcloud.co/apps/icons/screenly_1774968918600.png" alt="Screenly logo" width="28" height="28"> Screenly: Universal API

Manage digital signs, playlists, assets, and screen health

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/screenly/latest
- **Category:** Website & App Building / CMS
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://screenly.io
- **Vendor API docs:** https://developer.screenly.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | POST | Creates a new asset in Screenly. |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an existing asset from Screenly. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from Screenly. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from Screenly. |
| [Update Asset](actions/update-asset.md) | PUT | Updates an existing asset in Screenly. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Screenly. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Screenly. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Screenly. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Screenly. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Screenly. |

### Playlist

| Action | Method | Description |
| --- | --- | --- |
| [Create Playlist](actions/create-playlist.md) | POST | Creates a new playlist in Screenly. |
| [Delete Playlist](actions/delete-playlist.md) | DELETE | Deletes an existing playlist from Screenly. |
| [Get Playlist](actions/get-playlist.md) | GET | Retrieves a playlist from Screenly. |
| [List Playlists](actions/list-playlists.md) | GET | Retrieves playlists from Screenly. |
| [Update Playlist](actions/update-playlist.md) | PUT | Updates an existing playlist in Screenly. |

### Screen

| Action | Method | Description |
| --- | --- | --- |
| [List Screens](actions/list-screens.md) | GET | Retrieves screens from Screenly. |

