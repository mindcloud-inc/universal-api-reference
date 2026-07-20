# AddEvent: Native API Reference

A consolidated summary of AddEvent's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.addevent.com/
- **API base URL:** `https://api.addevent.com/calevent/v2`

## Authentication

### API Key

Use your AddEvent API token as a bearer token. Protected endpoints should be validated with a protected action, not List timezones.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.addevent.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.total_pages`. The current page number is read from `pagination.current_page`.

## Pagination

Use `page_size` in the query string to set the page size (default 10; accepted range 1–20). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create calendar](actions/create-calendar.md) | `POST /calendars` | [docs](https://docs.addevent.com/reference/create-calendar) |
| [Create event](actions/create-event.md) | `POST /events` | [docs](https://docs.addevent.com/reference/create-event) |
| [Create RSVP attendee](actions/create-rsvp-attendee.md) | `POST /events/:event_id/rsvps` | [docs](https://docs.addevent.com/reference/create-rsvp-attendee) |
| [Delete calendar](actions/delete-calendar.md) | `DELETE /calendars/:calendar_id` | [docs](https://docs.addevent.com/reference/delete-calendar) |
| [Delete calendar subscriber](actions/delete-calendar-subscriber.md) | `DELETE /subscribers/:subscriber_id` | [docs](https://docs.addevent.com/reference/delete-calendar-subscriber) |
| [Delete event](actions/delete-event.md) | `DELETE /events/:event_id` | [docs](https://docs.addevent.com/reference/delete-event) |
| [Delete RSVP attendee](actions/delete-rsvp-attendee.md) | `DELETE /rsvps/:attendee_id` | [docs](https://docs.addevent.com/reference/delete-rsvp-attendee) |
| [List calendar templates](actions/list-calendar-templates.md) | `GET /calendars/templates` | [docs](https://docs.addevent.com/reference/list-calendar-templates) |
| [List event templates](actions/list-event-templates.md) | `GET /events/templates` | [docs](https://docs.addevent.com/reference/list-event-templates) |
| [List RSVP forms](actions/list-rsvp-forms.md) | `GET /events/rsvp-forms` | [docs](https://docs.addevent.com/reference/list-rsvp-forms) |
| [List timezones](actions/list-timezones.md) | `GET /timezones` | [docs](https://docs.addevent.com/reference/list-timezones) |
| [Retrieve calendar](actions/retrieve-calendar.md) | `GET /calendars/:calendar_id` | [docs](https://docs.addevent.com/reference/retrieve-calendar) |
| [Retrieve calendar subscriber](actions/retrieve-calendar-subscriber.md) | `GET /subscribers/:subscriber_id` | [docs](https://docs.addevent.com/reference/retrieve-calendar-subscriber) |
| [Retrieve event](actions/retrieve-event.md) | `GET /events/:event_id` | [docs](https://docs.addevent.com/reference/retrieve-event) |
| [Retrieve RSVP attendee](actions/retrieve-rsvp-attendee.md) | `GET /rsvps/:attendee_id` | [docs](https://docs.addevent.com/reference/retrieve-rsvp-attendee) |
| [Search calendar subscribers](actions/search-calendar-subscribers.md) | `GET /subscribers` | [docs](https://docs.addevent.com/reference/search-calendar-subscribers) |
| [Search calendars](actions/search-calendars.md) | `GET /calendars` | [docs](https://docs.addevent.com/reference/search-calendars) |
| [Search events](actions/search-events.md) | `GET /events` | [docs](https://docs.addevent.com/reference/search-events) |
| [Search RSVP attendees](actions/search-rsvp-attendees.md) | `GET /rsvps` | [docs](https://docs.addevent.com/reference/search-rsvp-attendees) |
| [Update calendar](actions/update-calendar.md) | `PATCH /calendars/:calendar_id` | [docs](https://docs.addevent.com/reference/update-calendar) |
| [Update event](actions/update-event.md) | `PATCH /events/:event_id` | [docs](https://docs.addevent.com/reference/update-event) |
| [Update RSVP attendee](actions/update-rsvp-attendee.md) | `PATCH /rsvps/:attendee_id` | [docs](https://docs.addevent.com/reference/update-rsvp-attendee) |
