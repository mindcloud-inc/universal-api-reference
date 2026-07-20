# <img src="https://images.mindcloud.co/apps/icons/audius_1775682908049.png" alt="Audius logo" width="28" height="28"> Audius: Universal API

Stream tracks, manage playlists, and explore Audius artists and fans

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/audius/latest
- **Category:** Marketing / Social Media
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://audius.co/
- **Vendor API docs:** https://docs.audius.co/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Developer App](actions/get-developer-app.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audius/latest/actions/get-developer-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Track Comments](actions/get-track-comments.md) | GET | Retrieves comments for an Audius track. |

### Developer App

| Action | Method | Description |
| --- | --- | --- |
| [Get Developer App](actions/get-developer-app.md) | GET | Retrieves a developer app from Audius by address. |
| [Register API Key](actions/register-api-key.md) | POST | Creates API key credentials for an Audius developer app. |

### Playlist

| Action | Method | Description |
| --- | --- | --- |
| [Get Playlist](actions/get-playlist.md) | GET | Retrieves a playlist from Audius by ID. |

### Playlists

| Action | Method | Description |
| --- | --- | --- |
| [Get Trending Playlists](actions/get-trending-playlists.md) | GET | Retrieves trending playlists from Audius. |
| [Get User Playlists](actions/get-user-playlists.md) | GET | Retrieves playlists created by an Audius user. |
| [Search Playlists](actions/search-playlists.md) | GET | Finds playlists in Audius by query. |

### Track

| Action | Method | Description |
| --- | --- | --- |
| [Get Track](actions/get-track.md) | GET | Retrieves a track from Audius by ID. |

### Tracks

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Tracks](actions/get-latest-tracks.md) | GET | Retrieves latest tracks from Audius. |
| [Get Playlist Tracks](actions/get-playlist-tracks.md) | GET | Retrieves tracks in an Audius playlist. |
| [Get Track Remixes](actions/get-track-remixes.md) | GET | Retrieves remixes of an Audius track. |
| [Get Trending Tracks](actions/get-trending-tracks.md) | GET | Retrieves trending tracks from Audius. |
| [Get User Tracks](actions/get-user-tracks.md) | GET | Retrieves tracks created by an Audius user. |
| [Search Tracks](actions/search-tracks.md) | GET | Finds tracks in Audius by query. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Audius by ID. |
| [Get User by Handle](actions/get-user-by-handle.md) | GET | Retrieves a user from Audius by handle. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Users](actions/get-top-users.md) | GET | Retrieves top users from Audius. |
| [Get User Followers](actions/get-user-followers.md) | GET | Retrieves followers of an Audius user. |
| [Get User Following](actions/get-user-following.md) | GET | Retrieves users followed by an Audius user. |
| [Search Users](actions/search-users.md) | GET | Finds users in Audius by query. |

