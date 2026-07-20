# tl:dv: Native API Reference

A consolidated summary of tl:dv's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://doc.tldv.io/index.html
- **API base URL:** `https://pasta.tldv.io`

## Authentication

### API Key

Use a tl:dv API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://doc.tldv.io/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `results`. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Highlights](actions/get-highlights.md) | `GET /v1alpha1/meetings/:meetingId/highlights` | [docs](https://doc.tldv.io/index.html#tag/Highlights-(deprecated)/operation/GetHighlightsByMeetingId.getHighlightsByMeetingId) |
| [Get Meeting](actions/get-meeting.md) | `GET /v1alpha1/meetings/:meetingId` | [docs](https://doc.tldv.io/index.html#tag/Meetings/operation/GetMeetingById.GetMeetingById) |
| [Get Transcript](actions/get-transcript.md) | `GET /v1alpha1/meetings/:meetingId/transcript` | [docs](https://doc.tldv.io/index.html#tag/Transcripts/operation/GetTranscriptByMeetingId.GetTranscriptByMeetingId) |
| [Import Meeting](actions/import-meeting.md) | `POST /v1alpha1/meetings/import` | [docs](https://doc.tldv.io/index.html#tag/Meetings/operation/ImportController.ImportMeeting) |
| [List Meetings](actions/list-meetings.md) | `GET /v1alpha1/meetings` | [docs](https://doc.tldv.io/index.html#tag/Meetings/operation/GetMeetings.GetMeetingById) |
