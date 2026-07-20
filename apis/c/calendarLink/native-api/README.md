# CalendarLink: Native API Reference

A consolidated summary of CalendarLink's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3
- **OpenAPI specification:** https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3
- **API base URL:** `https://my.calendarlink.com/api/v1`

## Authentication

### API Key

Bearer token authentication for the CalendarLink REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://calendarlink.com/llm-create-add-to-calendar-event-instructions)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `meta.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | `POST /:organisation/event` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [Get Contact](actions/get-contact.md) | `GET /:organisation/contact/:contact` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [Get Event](actions/get-event.md) | `GET /:organisation/event/:event` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [List Collections](actions/list-collections.md) | `GET /:organisation/collection` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [List Contacts](actions/list-contacts.md) | `GET /:organisation/contact` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [List Event Registrations](actions/list-event-registrations.md) | `GET /:organisation/event/:event/registration` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [List Events](actions/list-events.md) | `GET /:organisation/event` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
| [List Past Events](actions/list-past-events.md) | `GET /:organisation/event/past` | [docs](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3) |
