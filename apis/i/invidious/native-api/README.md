# Invidious: Native API Reference

A consolidated summary of Invidious's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.invidious.io/api/
- **API base URL:** `{instanceUrl}/api/v1`

## Authentication

### Invidious Bearer Token

Bearer token for authenticated Invidious /api/v1/auth endpoints. Public endpoints can use the same connection instance URL without additional scopes.

### Credentials

- **API Key:** `apiKey` · required
- **Instance URL:** `instanceUrl` · required · Base URL of the Invidious instance to use, for example https://inv.nadeko.net. Use an official listed instance or a customer/self-hosted instance.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.invidious.io/api/authenticated-endpoints/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hl` | query | `string` | no | Optional response language for JSON responses, using Invidious language codes. |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Auth Subscription](actions/add-auth-subscription.md) | `POST /auth/subscriptions/:ucid` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Add Video To Auth Playlist](actions/add-video-to-auth-playlist.md) | `POST /auth/playlists/:id/videos` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Create Auth Playlist](actions/create-auth-playlist.md) | `POST /auth/playlists` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Delete Auth Playlist](actions/delete-auth-playlist.md) | `DELETE /auth/playlists/:id` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Get Auth Feed](actions/get-auth-feed.md) | `GET /auth/feed` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Get Auth Playlist](actions/get-auth-playlist.md) | `GET /auth/playlists/:id` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Get Auth Preferences](actions/get-auth-preferences.md) | `GET /auth/preferences` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:id` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Community](actions/get-channel-community.md) | `GET /channels/:id/community` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Latest Videos](actions/get-channel-latest-videos.md) | `GET /channels/:id/latest` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Playlists](actions/get-channel-playlists.md) | `GET /channels/:id/playlists` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Podcasts](actions/get-channel-podcasts.md) | `GET /channels/:id/podcasts` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Related Channels](actions/get-channel-related-channels.md) | `GET /channels/:id/channels` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Releases](actions/get-channel-releases.md) | `GET /channels/:id/releases` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Shorts](actions/get-channel-shorts.md) | `GET /channels/:id/shorts` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Streams](actions/get-channel-streams.md) | `GET /channels/:id/streams` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Channel Videos](actions/get-channel-videos.md) | `GET /channels/:id/videos` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Clip](actions/get-clip.md) | `GET /clips` | [docs](https://docs.invidious.io/api/) |
| [Get Community Post](actions/get-community-post.md) | `GET /post/:id` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Community Post Comments](actions/get-community-post-comments.md) | `GET /post/:id/comments` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Get Hashtag Results](actions/get-hashtag-results.md) | `GET /hashtag/:tag` | [docs](https://docs.invidious.io/api/) |
| [Get Mix](actions/get-mix.md) | `GET /mixes/:rdid` | [docs](https://docs.invidious.io/api/) |
| [Get Playlist](actions/get-playlist.md) | `GET /playlists/:plid` | [docs](https://docs.invidious.io/api/) |
| [Get Popular Videos](actions/get-popular-videos.md) | `GET /popular` | [docs](https://docs.invidious.io/api/) |
| [Get Search Suggestions](actions/get-search-suggestions.md) | `GET /search/suggestions` | [docs](https://docs.invidious.io/api/) |
| [Get Stats](actions/get-stats.md) | `GET /stats` | [docs](https://docs.invidious.io/api/) |
| [Get Trending Videos](actions/get-trending-videos.md) | `GET /trending` | [docs](https://docs.invidious.io/api/) |
| [Get Video](actions/get-video.md) | `GET /videos/:id` | [docs](https://docs.invidious.io/api/) |
| [Get Video Annotations](actions/get-video-annotations.md) | `GET /annotations/:id` | [docs](https://docs.invidious.io/api/) |
| [Get Video Captions](actions/get-video-captions.md) | `GET /captions/:id` | [docs](https://docs.invidious.io/api/) |
| [Get Video Comments](actions/get-video-comments.md) | `GET /comments/:id` | [docs](https://docs.invidious.io/api/) |
| [List Auth Playlists](actions/list-auth-playlists.md) | `GET /auth/playlists` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [List Auth Subscriptions](actions/list-auth-subscriptions.md) | `GET /auth/subscriptions` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Remove Auth Subscription](actions/remove-auth-subscription.md) | `DELETE /auth/subscriptions/:ucid` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Remove Video From Auth Playlist](actions/remove-video-from-auth-playlist.md) | `DELETE /auth/playlists/:id/videos/:index` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Resolve URL](actions/resolve-url.md) | `GET /resolveurl` | [docs](https://docs.invidious.io/api/) |
| [Search Channel](actions/search-channel.md) | `GET /channels/:ucid/search` | [docs](https://docs.invidious.io/api/channels_endpoint/) |
| [Search Videos And Channels](actions/search-videos-and-channels.md) | `GET /search` | [docs](https://docs.invidious.io/api/) |
| [Update Auth Playlist](actions/update-auth-playlist.md) | `PATCH /auth/playlists/:id` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
| [Update Auth Preferences](actions/update-auth-preferences.md) | `POST /auth/preferences` | [docs](https://docs.invidious.io/api/authenticated-endpoints/) |
