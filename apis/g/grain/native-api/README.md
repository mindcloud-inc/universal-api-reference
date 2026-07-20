# Grain: Native API Reference

A consolidated summary of Grain's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.grain.com/
- **API base URL:** `https://api.grain.com/_/public-api`

## Authentication

### Personal Access Token

Use a Grain personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.grain.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `cursor`.

## Pagination

Use `cursor` in the request body as the pagination cursor.

## Filtering

Send filters in the request body. Supported operators: `eq`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag to Recording](actions/add-tag-to-recording.md) | `PUT /v2/recordings/:recording_id/tags` | [docs](https://developers.grain.com/) |
| [Create Hook](actions/create-hook.md) | `POST /v2/hooks/create` | [docs](https://developers.grain.com/) |
| [Delete Hook](actions/delete-hook.md) | `DELETE /v2/hooks/:hook_id` | [docs](https://developers.grain.com/) |
| [Download Recording](actions/download-recording.md) | `GET /v2/recordings/:recording_id/download` | [docs](https://developers.grain.com/) |
| [Get Recording](actions/get-recording.md) | `POST /v2/recordings/:recording_id` | [docs](https://developers.grain.com/) |
| [Get Recording Transcript JSON](actions/get-recording-transcript-json.md) | `GET /v2/recordings/:recording_id/transcript` | [docs](https://developers.grain.com/) |
| [Get Recording Transcript SRT](actions/get-recording-transcript-srt.md) | `GET /v2/recordings/:recording_id/transcript.srt` | [docs](https://developers.grain.com/) |
| [Get Recording Transcript TXT](actions/get-recording-transcript-txt.md) | `GET /v2/recordings/:recording_id/transcript.txt` | [docs](https://developers.grain.com/) |
| [Get Recording Transcript VTT](actions/get-recording-transcript-vtt.md) | `GET /v2/recordings/:recording_id/transcript.vtt` | [docs](https://developers.grain.com/) |
| [List Hooks](actions/list-hooks.md) | `POST /v2/hooks` | [docs](https://developers.grain.com/) |
| [List Meeting Types](actions/list-meeting-types.md) | `POST /v2/meeting_types` | [docs](https://developers.grain.com/) |
| [List Recordings](actions/list-recordings.md) | `POST /v2/recordings` | [docs](https://developers.grain.com/) |
| [List Teams](actions/list-teams.md) | `POST /v2/teams` | [docs](https://developers.grain.com/) |
| [List Users](actions/list-users.md) | `POST /v2/users` | [docs](https://developers.grain.com/) |
| [Remove Tag from Recording](actions/remove-tag-from-recording.md) | `DELETE /v2/recordings/:recording_id/tags/:tag` | [docs](https://developers.grain.com/) |
| [Share Recording to Team](actions/share-recording-to-team.md) | `PUT /v2/recordings/:recording_id/teams/:team_id` | [docs](https://developers.grain.com/) |
| [Share Recording to User](actions/share-recording-to-user.md) | `PUT /v2/recordings/:recording_id/users` | [docs](https://developers.grain.com/) |
| [Unshare Recording from Team](actions/unshare-recording-from-team.md) | `DELETE /v2/recordings/:recording_id/teams/:team_id` | [docs](https://developers.grain.com/) |
| [Unshare Recording from User](actions/unshare-recording-from-user.md) | `DELETE /v2/recordings/:recording_id/users/:user_id` | [docs](https://developers.grain.com/) |
| [Update Recording](actions/update-recording.md) | `PATCH /v2/recordings/:recording_id` | [docs](https://developers.grain.com/) |
