# Twitch: Native API Reference

A consolidated summary of Twitch's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://dev.twitch.tv/docs/api
- **API base URL:** `https://api.twitch.tv/helix`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://id.twitch.tv/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://id.twitch.tv/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `channel:manage:broadcast channel:manage:polls channel:manage:predictions channel:manage:redemptions channel:manage:schedule clips:edit moderator:manage:chat_settings moderator:read:chatters user:read:follows channel:read:editors channel:read:stream_key moderator:read:followers`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://id.twitch.tv/oauth2/token.

[Official authentication documentation](https://dev.twitch.tv/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `first` in the query string to set the page size (maximum 100). Use `after` in the query string as the pagination cursor.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Channel Stream Schedule Segment](actions/create-channel-stream-schedule-segment.md) | `POST /schedule/segment` | [docs](https://dev.twitch.tv/docs/api/reference#create-channel-stream-schedule-segment) |
| [Create Clip](actions/create-clip.md) | `POST /clips` | [docs](https://dev.twitch.tv/docs/api/reference#create-clip) |
| [Create Custom Rewards](actions/create-custom-rewards.md) | `POST /channel_points/custom_rewards` | [docs](https://dev.twitch.tv/docs/api/reference#create-custom-rewards) |
| [Create Poll](actions/create-poll.md) | `POST /polls` | [docs](https://dev.twitch.tv/docs/api/reference#create-poll) |
| [Create Prediction](actions/create-prediction.md) | `POST /predictions` | [docs](https://dev.twitch.tv/docs/api/reference#create-prediction) |
| [Delete Channel Stream Schedule Segment](actions/delete-channel-stream-schedule-segment.md) | `DELETE /schedule/segment` | [docs](https://dev.twitch.tv/docs/api/reference#delete-channel-stream-schedule-segment) |
| [Delete Custom Reward](actions/delete-custom-reward.md) | `DELETE /channel_points/custom_rewards` | [docs](https://dev.twitch.tv/docs/api/reference#delete-custom-reward) |
| [End Poll](actions/end-poll.md) | `PATCH /polls` | [docs](https://dev.twitch.tv/docs/api/reference#end-poll) |
| [End Prediction](actions/end-prediction.md) | `PATCH /predictions` | [docs](https://dev.twitch.tv/docs/api/reference#end-prediction) |
| [Get Channel Stream Schedule](actions/get-channel-stream-schedule.md) | `GET /schedule` | [docs](https://dev.twitch.tv/docs/api/reference#get-channel-stream-schedule) |
| [Get Chat Settings](actions/get-chat-settings.md) | `GET /chat/settings` | [docs](https://dev.twitch.tv/docs/api/reference#get-chat-settings) |
| [Get Stream Key](actions/get-stream-key.md) | `GET /streams/key` | [docs](https://dev.twitch.tv/docs/api/reference#get-stream-key) |
| [List Channel Editors](actions/list-channel-editors.md) | `GET /channels/editors` | [docs](https://dev.twitch.tv/docs/api/reference#get-channel-editors) |
| [List Channel Emotes](actions/list-channel-emotes.md) | `GET /chat/emotes` | [docs](https://dev.twitch.tv/docs/api/reference#get-channel-emotes) |
| [List Channel Followers](actions/list-channel-followers.md) | `GET /channels/followers` | [docs](https://dev.twitch.tv/docs/api/reference#get-channel-followers) |
| [List Channel Information](actions/list-channel-information.md) | `GET /channels` | [docs](https://dev.twitch.tv/docs/api/reference#get-channel-information) |
| [List Chatters](actions/list-chatters.md) | `GET /chat/chatters` | [docs](https://dev.twitch.tv/docs/api/reference#get-chatters) |
| [List Clips](actions/list-clips.md) | `GET /clips` | [docs](https://dev.twitch.tv/docs/api/reference#get-clips) |
| [List Custom Rewards](actions/list-custom-rewards.md) | `GET /channel_points/custom_rewards` | [docs](https://dev.twitch.tv/docs/api/reference#get-custom-reward) |
| [List Followed Channels](actions/list-followed-channels.md) | `GET /channels/followed` | [docs](https://dev.twitch.tv/docs/api/reference#get-followed-channels) |
| [List Followed Streams](actions/list-followed-streams.md) | `GET /streams/followed` | [docs](https://dev.twitch.tv/docs/api/reference#get-followed-streams) |
| [List Games](actions/list-games.md) | `GET /games` | [docs](https://dev.twitch.tv/docs/api/reference#get-games) |
| [List Polls](actions/list-polls.md) | `GET /polls` | [docs](https://dev.twitch.tv/docs/api/reference#get-polls) |
| [List Predictions](actions/list-predictions.md) | `GET /predictions` | [docs](https://dev.twitch.tv/docs/api/reference#get-predictions) |
| [List Streams](actions/list-streams.md) | `GET /streams` | [docs](https://dev.twitch.tv/docs/api/reference#get-streams) |
| [List Top Games](actions/list-top-games.md) | `GET /games/top` | [docs](https://dev.twitch.tv/docs/api/reference#get-top-games) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://dev.twitch.tv/docs/api/reference#get-users) |
| [List Videos](actions/list-videos.md) | `GET /videos` | [docs](https://dev.twitch.tv/docs/api/reference#get-videos) |
| [Modify Channel Information](actions/modify-channel-information.md) | `PATCH /channels` | [docs](https://dev.twitch.tv/docs/api/reference#modify-channel-information) |
| [Search Categories](actions/search-categories.md) | `GET /search/categories` | [docs](https://dev.twitch.tv/docs/api/reference#search-categories) |
| [Search Channels](actions/search-channels.md) | `GET /search/channels` | [docs](https://dev.twitch.tv/docs/api/reference#search-channels) |
| [Update Channel Stream Schedule Segment](actions/update-channel-stream-schedule-segment.md) | `PATCH /schedule/segment` | [docs](https://dev.twitch.tv/docs/api/reference#update-channel-stream-schedule-segment) |
| [Update Chat Settings](actions/update-chat-settings.md) | `PATCH /chat/settings` | [docs](https://dev.twitch.tv/docs/api/reference#update-chat-settings) |
