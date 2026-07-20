# YouTube: Native API Reference

A consolidated summary of YouTube's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/youtube/v3
- **API base URL:** `https://www.googleapis.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/youtube https://www.googleapis.com/auth/youtube.force-ssl`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/youtube/v3/guides/auth/server-side-web-apps)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `maxResults` in the query string to set the page size (default 5; accepted range 0–50). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Playlist](actions/create-playlist.md) | `POST /youtube/v3/playlists` | [docs](https://developers.google.com/youtube/v3/docs/playlists/insert) |
| [Delete Video](actions/delete-video.md) | `DELETE /youtube/v3/videos` | [docs](https://developers.google.com/youtube/v3/docs/videos/delete) |
| [Get Video Rating](actions/get-video-rating.md) | `GET /youtube/v3/videos/getRating` | [docs](https://developers.google.com/youtube/v3/docs/videos/getRating) |
| [List Activities](actions/list-activities.md) | `GET /youtube/v3/activities` | [docs](https://developers.google.com/youtube/v3/docs/activities/list) |
| [List Captions](actions/list-captions.md) | `GET /youtube/v3/captions` | [docs](https://developers.google.com/youtube/v3/docs/captions/list) |
| [List Channels](actions/list-channels.md) | `GET /youtube/v3/channels` | [docs](https://developers.google.com/youtube/v3/docs/channels/list) |
| [List Comment Threads](actions/list-comment-threads.md) | `GET /youtube/v3/commentThreads` | [docs](https://developers.google.com/youtube/v3/docs/commentThreads/list) |
| [List Comments](actions/list-comments.md) | `GET /youtube/v3/comments` | [docs](https://developers.google.com/youtube/v3/docs/comments/list) |
| [List Playlist Items](actions/list-playlist-items.md) | `GET /youtube/v3/playlistItems` | [docs](https://developers.google.com/youtube/v3/docs/playlistItems/list) |
| [List Playlists](actions/list-playlists.md) | `GET /youtube/v3/playlists` | [docs](https://developers.google.com/youtube/v3/docs/playlists/list) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /youtube/v3/subscriptions` | [docs](https://developers.google.com/youtube/v3/docs/subscriptions/list) |
| [List Video Categories](actions/list-video-categories.md) | `GET /youtube/v3/videoCategories` | [docs](https://developers.google.com/youtube/v3/docs/videoCategories/list) |
| [List Videos](actions/list-videos.md) | `GET /youtube/v3/videos` | [docs](https://developers.google.com/youtube/v3/docs/videos/list) |
| [Rate Video](actions/rate-video.md) | `POST /youtube/v3/videos/rate` | [docs](https://developers.google.com/youtube/v3/docs/videos/rate) |
| [Search Videos](actions/search-videos.md) | `GET /youtube/v3/search` | [docs](https://developers.google.com/youtube/v3/docs/search/list) |
| [Set Thumbnail](actions/set-thumbnail.md) | `POST /upload/youtube/v3/thumbnails/set` | [docs](https://developers.google.com/youtube/v3/docs/thumbnails/set) |
| [Update Channel](actions/update-channel.md) | `PUT /youtube/v3/channels` | [docs](https://developers.google.com/youtube/v3/docs/channels/update) |
| [Update Playlist](actions/update-playlist.md) | `PUT /youtube/v3/playlists` | [docs](https://developers.google.com/youtube/v3/docs/playlists/update) |
| [Update Video](actions/update-video.md) | `PUT /youtube/v3/videos` | [docs](https://developers.google.com/youtube/v3/docs/videos/update) |
| [Upload Video](actions/upload-video.md) | `POST /upload/youtube/v3/videos` | [docs](https://developers.google.com/youtube/v3/docs/videos/insert) |
