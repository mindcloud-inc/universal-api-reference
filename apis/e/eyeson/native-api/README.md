# Eyeson: Native API Reference

A consolidated summary of Eyeson's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.eyeson.com/docs/rest/eyeson-api
- **API base URL:** `https://api.eyeson.team`

## Authentication

### API Key

Authenticate with an Eyeson API key sent as the raw Authorization header value.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.eyeson.com/docs/rest/eyeson-api)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Meeting Layer](actions/add-meeting-layer.md) | `POST /rooms/:accessKey/layers` | [docs](https://docs.eyeson.com/docs/rest/references/layers) |
| [Create Permalink](actions/create-permalink.md) | `POST /permalink` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [Delete Meeting Layer](actions/delete-meeting-layer.md) | `DELETE /rooms/:accessKey/layers/:index` | [docs](https://docs.eyeson.com/docs/rest/references/layers) |
| [Delete Permalink](actions/delete-permalink.md) | `DELETE /permalink/:permalinkId` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [End Meeting](actions/end-meeting.md) | `DELETE /rooms/:accessKey` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-room) |
| [Force Stop Meeting](actions/force-stop-meeting.md) | `DELETE /rooms/:roomId` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-room) |
| [Get Meeting Details](actions/get-meeting-details.md) | `GET /rooms/:accessKey` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-room) |
| [Get Meeting User](actions/get-meeting-user.md) | `GET /rooms/:accessKey/users/:userId` | [docs](https://docs.eyeson.com/docs/rest/references/user) |
| [Get Permalink](actions/get-permalink.md) | `GET /permalink/:permalinkId` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [Get Recording](actions/get-recording.md) | `GET /recordings/:recordingId` | [docs](https://docs.eyeson.com/docs/rest/references/recording) |
| [List Current Meetings](actions/list-current-meetings.md) | `GET /rooms` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-room) |
| [List Meeting Users](actions/list-meeting-users.md) | `GET /rooms/:accessKey/users` | [docs](https://docs.eyeson.com/docs/rest/references/user) |
| [List Permalinks](actions/list-permalinks.md) | `GET /permalink` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [Lock Meeting](actions/lock-meeting.md) | `POST /rooms/:accessKey/lock` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-room) |
| [Register Guest User](actions/register-guest-user.md) | `POST /guests/:guestToken` | [docs](https://docs.eyeson.com/docs/rest/references/user) |
| [Register Permalink Host User](actions/register-permalink-host-user.md) | `POST /permalink/:permalinkId/users` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [Remove Meeting User](actions/remove-meeting-user.md) | `DELETE /rooms/:accessKey/users/:userId` | [docs](https://docs.eyeson.com/docs/rest/references/user) |
| [Remove Permalink Host User](actions/remove-permalink-host-user.md) | `DELETE /permalink/:permalinkId/users/:userToken` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [Send Meeting Message](actions/send-meeting-message.md) | `POST /rooms/:accessKey/messages` | [docs](https://docs.eyeson.com/docs/rest/references/messages) |
| [Set Meeting Layout](actions/set-meeting-layout.md) | `POST /rooms/:accessKey/layout` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-layout) |
| [Start Broadcast](actions/start-broadcast.md) | `POST /rooms/:accessKey/broadcasts` | [docs](https://docs.eyeson.com/docs/rest/references/broadcast) |
| [Start Meeting](actions/start-meeting.md) | `POST /rooms` | [docs](https://docs.eyeson.com/docs/rest/references/meeting-room) |
| [Start Meeting Playback](actions/start-meeting-playback.md) | `POST /rooms/:accessKey/playbacks` | [docs](https://docs.eyeson.com/docs/rest/references/playbacks) |
| [Start Permalink Meeting](actions/start-permalink-meeting.md) | `POST /permalink/:userToken` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
| [Start Recording](actions/start-recording.md) | `POST /rooms/:accessKey/recording` | [docs](https://docs.eyeson.com/docs/rest/references/recording) |
| [Stop Broadcast](actions/stop-broadcast.md) | `DELETE /rooms/:accessKey/broadcasts` | [docs](https://docs.eyeson.com/docs/rest/references/broadcast) |
| [Stop Meeting Playback](actions/stop-meeting-playback.md) | `DELETE /rooms/:accessKey/playbacks/:playId` | [docs](https://docs.eyeson.com/docs/rest/references/playbacks) |
| [Stop Recording](actions/stop-recording.md) | `DELETE /rooms/:accessKey/recording` | [docs](https://docs.eyeson.com/docs/rest/references/recording) |
| [Update Broadcast Player URL](actions/update-broadcast-player-url.md) | `PUT /rooms/:accessKey/broadcasts` | [docs](https://docs.eyeson.com/docs/rest/references/broadcast) |
| [Update Permalink](actions/update-permalink.md) | `PUT /permalink/:permalinkId` | [docs](https://docs.eyeson.com/docs/rest/references/permalink) |
