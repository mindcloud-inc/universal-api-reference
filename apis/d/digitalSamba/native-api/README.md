# Digital Samba: Native API Reference

A consolidated summary of Digital Samba's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.digitalsamba.com/reference/rest-api
- **OpenAPI specification:** https://developer.digitalsamba.com/rest-api/
- **API base URL:** `https://api.digitalsamba.com/api/v1`

## Authentication

### API Key

Authenticate Digital Samba REST API requests with a developer key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.digitalsamba.com/dashboard/getting-started/authenticate-to-the-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive recording](actions/archive-recording.md) | `POST /recordings/:recording/archive` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-POSTapi-v1-recordings--recording--archive) |
| [Create a new role](actions/create-a-new-role.md) | `POST /roles` | [docs](https://developer.digitalsamba.com/rest-api/#roles-POSTapi-v1-roles) |
| [Create a new room](actions/create-a-new-room.md) | `POST /rooms` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms) |
| [Create a question in the room](actions/create-a-question-in-the-room.md) | `POST /rooms/:room/questions` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms--room--questions) |
| [Create room token](actions/create-room-token.md) | `POST /rooms/:room/token` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms--room--token) |
| [Delete room](actions/delete-room.md) | `DELETE /rooms/:room` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-DELETEapi-v1-rooms--room-) |
| [Download the specified recording](actions/download-the-specified-recording.md) | `GET /recordings/:recording/download` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings--recording--download) |
| [Get all participants](actions/get-all-participants.md) | `GET /participants` | [docs](https://developer.digitalsamba.com/rest-api/#participants-GETapi-v1-participants) |
| [Get all room participants](actions/get-all-room-participants.md) | `GET /rooms/:room/participants` | [docs](https://developer.digitalsamba.com/rest-api/#participants-GETapi-v1-rooms--room--participants) |
| [Get all room sessions](actions/get-all-room-sessions.md) | `GET /rooms/:room/sessions` | [docs](https://developer.digitalsamba.com/rest-api/#sessions-GETapi-v1-rooms--room--sessions) |
| [Get all session participants](actions/get-all-session-participants.md) | `GET /sessions/:session/participants` | [docs](https://developer.digitalsamba.com/rest-api/#participants-GETapi-v1-sessions--session--participants) |
| [Get all sessions](actions/get-all-sessions.md) | `GET /sessions` | [docs](https://developer.digitalsamba.com/rest-api/#sessions-GETapi-v1-sessions) |
| [Get all team recordings](actions/get-all-team-recordings.md) | `GET /recordings` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings) |
| [Get all team rooms](actions/get-all-team-rooms.md) | `GET /rooms` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms) |
| [Get archived team recordings](actions/get-archived-team-recordings.md) | `GET /recordings/archived` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings-archived) |
| [Get available libraries for the team](actions/get-available-libraries-for-the-team.md) | `GET /libraries` | [docs](https://developer.digitalsamba.com/rest-api/#libraries-GETapi-v1-libraries) |
| [Get available library files](actions/get-available-library-files.md) | `GET /libraries/:library/files` | [docs](https://developer.digitalsamba.com/rest-api/#libraries-GETapi-v1-libraries--library--files) |
| [Get available permissions for roles](actions/get-available-permissions-for-roles.md) | `GET /permissions` | [docs](https://developer.digitalsamba.com/rest-api/#permissions-GETapi-v1-permissions) |
| [Get available roles for the team](actions/get-available-roles-for-the-team.md) | `GET /roles` | [docs](https://developer.digitalsamba.com/rest-api/#roles-GETapi-v1-roles) |
| [Get bookmarks](actions/get-bookmarks.md) | `GET /recordings/:recording/bookmarks` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings--recording--bookmarks) |
| [Get chat messages](actions/get-chat-messages.md) | `GET /rooms/:room/chat` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room--chat) |
| [Get default room settings](actions/get-default-room-settings.md) | `GET /` | [docs](https://developer.digitalsamba.com/rest-api/#default-room-settings-GETapi-v1) |
| [Get participant statistics](actions/get-participant-statistics.md) | `GET /participants/:participant` | [docs](https://developer.digitalsamba.com/rest-api/#statistics-GETapi-v1-participants--participant--statistics) |
| [Get questions and answers](actions/get-questions-and-answers.md) | `GET /rooms/:room/questions` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room--questions) |
| [Get room transcripts](actions/get-room-transcripts.md) | `GET /rooms/:room/transcripts` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room--transcripts) |
| [Get rooms with live participants count](actions/get-rooms-with-live-participants-count.md) | `GET /rooms/live` | [docs](https://developer.digitalsamba.com/rest-api/#live-GETapi-v1-rooms-live) |
| [Get rooms with live participants data](actions/get-rooms-with-live-participants-data.md) | `GET /rooms/live/participants` | [docs](https://developer.digitalsamba.com/rest-api/#live-GETapi-v1-rooms-live-participants) |
| [Get session statistics](actions/get-session-statistics.md) | `GET /sessions/:session` | [docs](https://developer.digitalsamba.com/rest-api/#statistics-GETapi-v1-sessions--session--statistics) |
| [Get session summary](actions/get-session-summary.md) | `GET /sessions/:session/summary` | [docs](https://developer.digitalsamba.com/rest-api/#sessions-GETapi-v1-sessions--session--summary) |
| [Get session transcripts](actions/get-session-transcripts.md) | `GET /sessions/:session/transcripts` | [docs](https://developer.digitalsamba.com/rest-api/#sessions-GETapi-v1-sessions--session--transcripts) |
| [Get the specified library hierarchy](actions/get-the-specified-library-hierarchy.md) | `GET /libraries/:library/hierarchy` | [docs](https://developer.digitalsamba.com/rest-api/#libraries-GETapi-v1-libraries--library--hierarchy) |
| [Get the specified recording](actions/get-the-specified-recording.md) | `GET /recordings/:recording` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings--recording-) |
| [Get the specified role](actions/get-the-specified-role.md) | `GET /roles/:role` | [docs](https://developer.digitalsamba.com/rest-api/#roles-GETapi-v1-roles--role-) |
| [Get the specified room](actions/get-the-specified-room.md) | `GET /rooms/:room` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room-) |
| [Get webhooks for the team](actions/get-webhooks-for-the-team.md) | `GET /webhooks` | [docs](https://developer.digitalsamba.com/rest-api/#webhooks-GETapi-v1-webhooks) |
| [Send chat message](actions/send-chat-message.md) | `POST /rooms/:room/chat` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms--room--chat) |
| [Unarchive recording](actions/unarchive-recording.md) | `POST /recordings/:recording/unarchive` | [docs](https://developer.digitalsamba.com/rest-api/#recordings-POSTapi-v1-recordings--recording--unarchive) |
| [Update default room settings](actions/update-default-room-settings.md) | `PATCH /` | [docs](https://developer.digitalsamba.com/rest-api/#default-room-settings-PATCHapi-v1) |
| [Update room](actions/update-room.md) | `PATCH /rooms/:room` | [docs](https://developer.digitalsamba.com/rest-api/#rooms-PATCHapi-v1-rooms--room-) |
| [Update the specified role](actions/update-the-specified-role.md) | `PATCH /roles/:role` | [docs](https://developer.digitalsamba.com/rest-api/#roles-PATCHapi-v1-roles--role-) |
