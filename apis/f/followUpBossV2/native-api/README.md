# Follow Up Boss: Native API Reference

A consolidated summary of Follow Up Boss's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.followupboss.com/reference
- **API base URL:** `https://api.followupboss.com/v1/`

## Authentication

### Custom API Key

### Credentials

- **Basic Token:** `basicToken` · required · Paste the Base64-encoded value of api_key: without the Basic prefix.
- **System:** `system` · required · Enter the registered Follow Up Boss system name used in the X-System header.
- **System Key:** `systemSecret` · required · Enter the registered Follow Up Boss system key used in the X-System-Key header.

Send these headers with each API request:

```http
X-System: <system>
X-System-Key: <systemSecret>
```

[Official authentication documentation](https://docs.followupboss.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Duplicate Person](actions/check-duplicate-person.md) | `GET people/checkDuplicate` | [docs](https://docs.followupboss.com/reference/people-checkduplicate) |
| [Create Appointment](actions/create-appointment.md) | `POST appointments` | [docs](https://docs.followupboss.com/reference/appointments-post) |
| [Create Event](actions/create-event.md) | `POST events` | [docs](https://docs.followupboss.com/reference/events-post) |
| [Create Note](actions/create-note.md) | `POST notes` | [docs](https://docs.followupboss.com/reference/notes-post) |
| [Create Person](actions/create-person.md) | `POST people` | [docs](https://docs.followupboss.com/reference/people-post) |
| [Create Task](actions/create-task.md) | `POST tasks` | [docs](https://docs.followupboss.com/reference/tasks-post) |
| [Get Appointment](actions/get-appointment.md) | `GET appointments/:id` | [docs](https://docs.followupboss.com/reference/appointments-id-get) |
| [Get Current User](actions/get-current-user.md) | `GET me` | [docs](https://docs.followupboss.com/reference/me) |
| [Get Event](actions/get-event.md) | `GET events/:id` | [docs](https://docs.followupboss.com/reference/events-id-get) |
| [Get Note](actions/get-note.md) | `GET notes/:id` | [docs](https://docs.followupboss.com/reference/notes-id-get) |
| [Get Person](actions/get-person.md) | `GET people/:id` | [docs](https://docs.followupboss.com/reference/people-id-get) |
| [Get Task](actions/get-task.md) | `GET tasks/:id` | [docs](https://docs.followupboss.com/reference/tasks-id-get) |
| [Get User](actions/get-user.md) | `GET users/:id` | [docs](https://docs.followupboss.com/reference/users-id-get) |
| [List Appointments](actions/list-appointments.md) | `GET appointments` | [docs](https://docs.followupboss.com/reference/appointments-get) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET customFields` | [docs](https://docs.followupboss.com/reference/customfields-get) |
| [List Events](actions/list-events.md) | `GET events` | [docs](https://docs.followupboss.com/reference/events-get) |
| [List People](actions/list-people.md) | `GET people` | [docs](https://docs.followupboss.com/reference/people-get) |
| [List Tasks](actions/list-tasks.md) | `GET tasks` | [docs](https://docs.followupboss.com/reference/tasks-get) |
| [List Unclaimed People](actions/list-unclaimed-people.md) | `GET people/unclaimed` | [docs](https://docs.followupboss.com/reference/peopleunclaimed) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://docs.followupboss.com/reference/users-get) |
| [Update Appointment](actions/update-appointment.md) | `PUT appointments/:id` | [docs](https://docs.followupboss.com/reference/appointments-id-put) |
| [Update Note](actions/update-note.md) | `PUT notes/:id` | [docs](https://docs.followupboss.com/reference/notes-id-put) |
| [Update Person](actions/update-person.md) | `PUT people/:id` | [docs](https://docs.followupboss.com/reference/people-id-put) |
| [Update Task](actions/update-task.md) | `PUT tasks/:id` | [docs](https://docs.followupboss.com/reference/tasks-id-put) |
