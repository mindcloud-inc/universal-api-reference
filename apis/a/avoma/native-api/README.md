# Avoma: Native API Reference

A consolidated summary of Avoma's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://dev.avoma.com
- **OpenAPI specification:** https://dev.avoma.com/openapi.yml
- **API base URL:** `https://api.avoma.com`

## Authentication

### API Key

Use an Avoma API key for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.avoma.com/api-integration-for-avoma)

## Pagination

Use `page_size` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Sorting

Set the sort field with `o` in the query string. Use `start_at` for ascending order and `-start_at` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | `POST /v1/calls/` | [docs](https://dev.avoma.com) |
| [Create Meeting Outcome](actions/create-meeting-outcome.md) | `POST /v1/meeting_outcome/` | [docs](https://dev.avoma.com) |
| [Create Meeting Type](actions/create-meeting-type.md) | `POST /v1/meeting_type/` | [docs](https://dev.avoma.com) |
| [Delete Meeting Outcome](actions/delete-meeting-outcome.md) | `DELETE /v1/meeting_outcome/:uuid/` | [docs](https://dev.avoma.com) |
| [Delete Meeting Type](actions/delete-meeting-type.md) | `DELETE /v1/meeting_type/:uuid/` | [docs](https://dev.avoma.com) |
| [Get Call](actions/get-call.md) | `GET /v1/calls/:external_id/` | [docs](https://dev.avoma.com) |
| [Get Meeting](actions/get-meeting.md) | `GET /v1/meetings/:uuid/` | [docs](https://dev.avoma.com) |
| [Get Meeting Insights](actions/get-meeting-insights.md) | `GET /v1/meetings/:meetingUuid/insights/` | [docs](https://dev.avoma.com) |
| [Get Meeting Outcome](actions/get-meeting-outcome.md) | `GET /v1/meeting_outcome/:uuid/` | [docs](https://dev.avoma.com) |
| [Get Meeting Segments](actions/get-meeting-segments.md) | `GET /v1/meeting_segments/` | [docs](https://dev.avoma.com) |
| [Get Meeting Sentiments](actions/get-meeting-sentiments.md) | `GET /v1/meeting_sentiments/` | [docs](https://dev.avoma.com) |
| [Get Meeting Type](actions/get-meeting-type.md) | `GET /v1/meeting_type/:uuid/` | [docs](https://dev.avoma.com) |
| [Get Recording](actions/get-recording.md) | `GET /v1/recordings/` | [docs](https://dev.avoma.com) |
| [Get Recording By UUID](actions/get-recording-by-uuid.md) | `GET /v1/recordings/:uuid/` | [docs](https://dev.avoma.com) |
| [Get Transcription](actions/get-transcription.md) | `GET /v1/transcriptions/:uuid/` | [docs](https://dev.avoma.com) |
| [List Calls](actions/list-calls.md) | `GET /v1/calls/` | [docs](https://dev.avoma.com) |
| [List Meeting Outcomes](actions/list-meeting-outcomes.md) | `GET /v1/meeting_outcome/` | [docs](https://dev.avoma.com) |
| [List Meeting Types](actions/list-meeting-types.md) | `GET /v1/meeting_type/` | [docs](https://dev.avoma.com) |
| [List Meetings](actions/list-meetings.md) | `GET /v1/meetings/` | [docs](https://dev.avoma.com) |
| [List Notes](actions/list-notes.md) | `GET /v1/notes/` | [docs](https://dev.avoma.com) |
| [List Transcriptions](actions/list-transcriptions.md) | `GET /v1/transcriptions/` | [docs](https://dev.avoma.com) |
| [List Users](actions/list-users.md) | `GET /v1/users/` | [docs](https://dev.avoma.com) |
| [Update Call](actions/update-call.md) | `PATCH /v1/calls/:external_id/` | [docs](https://dev.avoma.com) |
| [Update Meeting Outcome](actions/update-meeting-outcome.md) | `PATCH /v1/meeting_outcome/:uuid/` | [docs](https://dev.avoma.com) |
| [Update Meeting Type](actions/update-meeting-type.md) | `PATCH /v1/meeting_type/:uuid/` | [docs](https://dev.avoma.com) |
