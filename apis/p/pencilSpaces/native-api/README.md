# Pencil Spaces: Native API Reference

A consolidated summary of Pencil Spaces's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://api.pencilspaces.com/guide
- **OpenAPI specification:** https://api.swaggerhub.com/apis/Pencil/pencil-spaces-api/1.1.0/swagger.json
- **API base URL:** `https://apis.pencilapp.com/public/api`

## Authentication

### API Key

Authenticate with a Pencil Spaces API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.pencilspaces.com/guide/generating-your-key)

## API conventions

Responses from this API use JSON. The total page count is read from `totalPages`. The current page number is read from `pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size. Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://api.pencilspaces.com/guide/events) |
| [Create Space](actions/create-space.md) | `POST /spaces/create` | [docs](https://api.pencilspaces.com/guide/spaces) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/:eventId` | [docs](https://api.pencilspaces.com/guide/events) |
| [Delete Session](actions/delete-session.md) | `DELETE /analytics/sessions/:sessionId` | [docs](https://api.pencilspaces.com/reference) |
| [Delete Space](actions/delete-space.md) | `DELETE /spaces/:spaceId` | [docs](https://api.pencilspaces.com/guide/spaces) |
| [End Ongoing Session](actions/end-ongoing-session.md) | `POST /spaces/:spaceId/endOngoingSession` | [docs](https://api.pencilspaces.com/reference) |
| [Get Audit History](actions/get-audit-history.md) | `GET /audit/:documentId` | [docs](https://api.pencilspaces.com/reference) |
| [Get Event](actions/get-event.md) | `GET /events/:eventId` | [docs](https://api.pencilspaces.com/guide/events) |
| [Get Session](actions/get-session.md) | `GET /analytics/sessions/:sessionId` | [docs](https://api.pencilspaces.com/reference) |
| [Get Space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://api.pencilspaces.com/guide/spaces) |
| [List Custom Attributes](actions/list-custom-attributes.md) | `GET /attributes` | [docs](https://api.pencilspaces.com/guide/data-model) |
| [List Sessions](actions/list-sessions.md) | `GET /analytics/sessions` | [docs](https://api.pencilspaces.com/reference) |
| [List Space Recordings](actions/list-space-recordings.md) | `GET /spaces/recordings/:spaceId` | [docs](https://api.pencilspaces.com/reference) |
| [List Spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://api.pencilspaces.com/guide/spaces) |
| [Update Event](actions/update-event.md) | `PUT /events/:eventId` | [docs](https://api.pencilspaces.com/guide/events) |
| [Update Space](actions/update-space.md) | `PATCH /spaces/:spaceId` | [docs](https://api.pencilspaces.com/guide/spaces) |
| [Update Space Settings](actions/update-space-settings.md) | `PATCH /spaces/:spaceId/settings/` | [docs](https://api.pencilspaces.com/guide/spaces) |
| [Update Space User Roles](actions/update-space-user-roles.md) | `PATCH /spaces/:spaceId/updateUsers` | [docs](https://api.pencilspaces.com/reference) |
