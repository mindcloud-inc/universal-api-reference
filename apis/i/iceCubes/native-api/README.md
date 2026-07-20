# IceCubes: Native API Reference

A consolidated summary of IceCubes's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://icecubes.app/docs/api/rest
- **API base URL:** `https://icecubes.app/api/public`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://icecubes.app/docs/api)

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

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Action Item](actions/create-action-item.md) | `POST /action-items` | [docs](https://icecubes.app/docs/api/rest) |
| [Get Meeting](actions/get-meeting.md) | `GET /meetings/:id` | [docs](https://icecubes.app/docs/api/rest) |
| [Get Meeting Insights](actions/get-meeting-insights.md) | `GET /meetings/:id/insights` | [docs](https://icecubes.app/docs/api/rest) |
| [Get Meeting Notes](actions/get-meeting-notes.md) | `GET /meetings/:id/notes` | [docs](https://icecubes.app/docs/api/rest) |
| [Get Meeting Transcript](actions/get-meeting-transcript.md) | `GET /meetings/:id/transcript` | [docs](https://icecubes.app/docs/api/rest) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://icecubes.app/docs/api/rest) |
| [List Action Items](actions/list-action-items.md) | `GET /action-items` | [docs](https://icecubes.app/docs/api/rest) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://icecubes.app/docs/api/rest) |
| [List Meetings](actions/list-meetings.md) | `GET /meetings` | [docs](https://icecubes.app/docs/api/rest) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://icecubes.app/docs/api/rest) |
| [Search Meeting Content](actions/search-meeting-content.md) | `GET /search` | [docs](https://icecubes.app/docs/api/rest) |
| [Update Action Item](actions/update-action-item.md) | `PATCH /action-items/:id` | [docs](https://icecubes.app/docs/api/rest) |
| [Update Meeting Notes](actions/update-meeting-notes.md) | `PUT /meetings/:id/notes` | [docs](https://icecubes.app/docs/api/rest) |
