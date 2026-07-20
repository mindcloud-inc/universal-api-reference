# Audius: Native API Reference

A consolidated summary of Audius's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.audius.co/api
- **OpenAPI specification:** https://api.audius.co/v1/swagger.yaml
- **API base URL:** `https://api.audius.co/v1`

## Authentication

### Developer App Key + Secret

Use the Audius developer app API key as the username and the developer app secret as the password. Enter the owner user ID as an additional field for protected developer-app operations.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **User ID:** `userId` · required · The Audius user ID that owns the developer app. Required for protected developer-app operations.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.audius.co/v1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Developer App](actions/get-developer-app.md) | `GET /developer-apps/:address` | [docs](https://api.audius.co/v1) |
| [Get Latest Tracks](actions/get-latest-tracks.md) | `GET /tracks/latest` | [docs](https://api.audius.co/v1) |
| [Get Playlist](actions/get-playlist.md) | `GET /playlists/:playlist_id` | [docs](https://api.audius.co/v1) |
| [Get Playlist Tracks](actions/get-playlist-tracks.md) | `GET /playlists/:playlist_id/tracks` | [docs](https://api.audius.co/v1) |
| [Get Top Users](actions/get-top-users.md) | `GET /users/top` | [docs](https://api.audius.co/v1) |
| [Get Track](actions/get-track.md) | `GET /tracks/:track_id` | [docs](https://api.audius.co/v1) |
| [Get Track Comments](actions/get-track-comments.md) | `GET /tracks/:track_id/comments` | [docs](https://api.audius.co/v1) |
| [Get Track Remixes](actions/get-track-remixes.md) | `GET /tracks/:track_id/remixes` | [docs](https://api.audius.co/v1) |
| [Get Trending Playlists](actions/get-trending-playlists.md) | `GET /playlists/trending` | [docs](https://api.audius.co/v1) |
| [Get Trending Tracks](actions/get-trending-tracks.md) | `GET /tracks/trending` | [docs](https://api.audius.co/v1) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://api.audius.co/v1) |
| [Get User by Handle](actions/get-user-by-handle.md) | `GET /users/handle/:handle` | [docs](https://api.audius.co/v1) |
| [Get User Followers](actions/get-user-followers.md) | `GET /users/:id/followers` | [docs](https://api.audius.co/v1) |
| [Get User Following](actions/get-user-following.md) | `GET /users/:id/following` | [docs](https://api.audius.co/v1) |
| [Get User Playlists](actions/get-user-playlists.md) | `GET /users/:id/playlists` | [docs](https://api.audius.co/v1) |
| [Get User Tracks](actions/get-user-tracks.md) | `GET /users/:id/tracks` | [docs](https://api.audius.co/v1) |
| [Register API Key](actions/register-api-key.md) | `POST /developer-apps/:address/register-api-key` | [docs](https://api.audius.co/v1) |
| [Search Playlists](actions/search-playlists.md) | `GET /playlists/search` | [docs](https://api.audius.co/v1) |
| [Search Tracks](actions/search-tracks.md) | `GET /tracks/search` | [docs](https://api.audius.co/v1) |
| [Search Users](actions/search-users.md) | `GET /users/search` | [docs](https://api.audius.co/v1) |
