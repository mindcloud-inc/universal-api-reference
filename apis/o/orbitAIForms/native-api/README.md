# Orbit AI (Forms): Native API Reference

A consolidated summary of Orbit AI (Forms)'s API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.orbitforms.ai/developers/api/overview
- **API base URL:** `https://orbitforms.ai`

## Authentication

### API Key

Use an Orbit AI API key to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.orbitforms.ai/developers/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.total_pages`. The current page number is read from `meta.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact to Sequence](actions/add-contact-to-sequence.md) | `POST /api/v1/sequences/:id/enrollments` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
| [Create Form](actions/create-form.md) | `POST /api/v1/forms` | [docs](https://docs.orbitforms.ai/developers/api/forms#endpoints) |
| [Create Meeting](actions/create-meeting.md) | `POST /api/calendar/book` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#book-a-meeting) |
| [Create Scheduling Page](actions/create-scheduling-page.md) | `POST /api/v1/scheduling-pages` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#create-a-scheduling-page) |
| [Create Scheduling Page Event Type](actions/create-scheduling-page-event-type.md) | `POST /api/v1/scheduling-pages/:id/event-types` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-2) |
| [Create Sequence](actions/create-sequence.md) | `POST /api/v1/sequences` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
| [Delete Form](actions/delete-form.md) | `DELETE /api/v1/forms/:id` | [docs](https://docs.orbitforms.ai/developers/api/forms#endpoints) |
| [Delete Scheduling Page](actions/delete-scheduling-page.md) | `DELETE /api/v1/scheduling-pages/:id` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints) |
| [Delete Scheduling Page Event Type](actions/delete-scheduling-page-event-type.md) | `DELETE /api/v1/scheduling-pages/:id/event-types/:eventTypeId` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-2) |
| [Delete Sequence](actions/delete-sequence.md) | `DELETE /api/v1/sequences/:id` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
| [Get Availability Schedule](actions/get-availability-schedule.md) | `GET /api/v1/availability-schedules/:id` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#get-availability-schedule) |
| [Get Form](actions/get-form.md) | `GET /api/v1/forms/:id` | [docs](https://docs.orbitforms.ai/developers/api/forms#get-form) |
| [Get Meeting](actions/get-meeting.md) | `GET /api/v1/meetings/:id` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-3) |
| [Get Scheduling Page](actions/get-scheduling-page.md) | `GET /api/v1/scheduling-pages/:id` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#get-scheduling-page) |
| [Get Scheduling Page Event Type](actions/get-scheduling-page-event-type.md) | `GET /api/v1/scheduling-pages/:id/event-types/:eventTypeId` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-2) |
| [Get Sequence](actions/get-sequence.md) | `GET /api/v1/sequences/:id` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
| [List Availability Schedules](actions/list-availability-schedules.md) | `GET /api/v1/availability-schedules` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-4) |
| [List Available Time Slots](actions/list-available-time-slots.md) | `GET /api/calendar/availability` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#get-available-time-slots) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /api/v1/forms/:id/submissions` | [docs](https://docs.orbitforms.ai/developers/api/submissions#endpoints) |
| [List Forms](actions/list-forms.md) | `GET /api/v1/forms` | [docs](https://docs.orbitforms.ai/developers/api/forms#list-forms) |
| [List Meetings](actions/list-meetings.md) | `GET /api/v1/meetings` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#list-meetings) |
| [List Scheduling Page Event Types](actions/list-scheduling-page-event-types.md) | `GET /api/v1/scheduling-pages/:id/event-types` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-2) |
| [List Scheduling Pages](actions/list-scheduling-pages.md) | `GET /api/v1/scheduling-pages` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#list-scheduling-pages) |
| [List Sequences](actions/list-sequences.md) | `GET /api/v1/sequences` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
| [Remove Contact from Sequence](actions/remove-contact-from-sequence.md) | `DELETE /api/v1/sequences/:id/enrollments` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
| [Update Form](actions/update-form.md) | `PATCH /api/v1/forms/:id` | [docs](https://docs.orbitforms.ai/developers/api/forms#endpoints) |
| [Update Meeting](actions/update-meeting.md) | `PATCH /api/v1/meetings/:id` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#update-a-meeting) |
| [Update Scheduling Page](actions/update-scheduling-page.md) | `PATCH /api/v1/scheduling-pages/:id` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints) |
| [Update Scheduling Page Event Type](actions/update-scheduling-page-event-type.md) | `PATCH /api/v1/scheduling-pages/:id/event-types/:eventTypeId` | [docs](https://docs.orbitforms.ai/developers/api/scheduling#endpoints-2) |
| [Update Sequence](actions/update-sequence.md) | `PATCH /api/v1/sequences/:id` | [docs](https://docs.orbitforms.ai/developers/api/sequences#available-endpoints) |
