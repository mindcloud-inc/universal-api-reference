# Mihu AI: Native API Reference

A consolidated summary of Mihu AI's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.mihu.ai/api-reference/introduction
- **OpenAPI specification:** https://app.mihu.ai/docs/api-docs.json
- **API base URL:** `https://{subdomain}.mindhunters.ai`

## Authentication

### API Key

Use a Mihu API token with a workspace subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace Subdomain:** `subdomain` · required · Your Mihu workspace subdomain, for example `mindcloudmihu`. This value is used to build the API base URL.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.mihu.ai/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `data.last_page`. The current page number is read from `data.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 15; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag to Contact](actions/add-tag-to-contact.md) | `POST /api/v1/contacts/:uuid/add-tag` | [docs](https://developers.mihu.ai/api-reference/contacts/add-tag-to-contact) |
| [Cancel a Task](actions/cancel-a-task.md) | `POST /api/v1/tasks/:uuid/cancel` | [docs](https://developers.mihu.ai/api-reference/tasks/cancel-a-task) |
| [Cancel an Appointment Request](actions/cancel-an-appointment-request.md) | `POST /api/v1/appointment-requests/:uuid/cancel` | [docs](https://developers.mihu.ai/api-reference/appointment-requests/cancel-an-appointment-request) |
| [Create a New Appointment](actions/create-a-new-appointment.md) | `POST /api/v1/appointments` | [docs](https://developers.mihu.ai/api-reference/appointments/create-a-new-appointment) |
| [Create a New Appointment Request](actions/create-a-new-appointment-request.md) | `POST /api/v1/appointment-requests` | [docs](https://developers.mihu.ai/api-reference/appointment-requests/create-a-new-appointment-request) |
| [Create a New Campaign](actions/create-a-new-campaign.md) | `POST /api/v1/campaigns` | [docs](https://developers.mihu.ai/api-reference/campaigns/create-a-new-campaign) |
| [Create a New Contact](actions/create-a-new-contact.md) | `POST /api/v1/contacts` | [docs](https://developers.mihu.ai/api-reference/contacts/create-a-new-contact) |
| [Create a New Schedule](actions/create-a-new-schedule.md) | `POST /api/v1/schedules` | [docs](https://developers.mihu.ai/api-reference/schedules/create-a-new-schedule) |
| [Create a New Task](actions/create-a-new-task.md) | `POST /api/v1/tasks` | [docs](https://developers.mihu.ai/api-reference/tasks/create-a-new-task-call-or-whatsapp-template) |
| [Create a New Transcription Request](actions/create-a-new-transcription-request.md) | `POST /api/v1/transcriptions` | [docs](https://developers.mihu.ai/api-reference/transcriptions/create-a-new-transcription-request) |
| [Delete a Campaign](actions/delete-a-campaign.md) | `DELETE /api/v1/campaigns/:uuid` | [docs](https://developers.mihu.ai/api-reference/campaigns/delete-a-campaign) |
| [Delete a Contact](actions/delete-a-contact.md) | `DELETE /api/v1/contacts/:uuid` | [docs](https://developers.mihu.ai/api-reference/contacts/delete-a-contact) |
| [Delete a Task](actions/delete-a-task.md) | `DELETE /api/v1/tasks/:uuid` | [docs](https://developers.mihu.ai/api-reference/tasks/delete-a-task) |
| [Delete an Appointment](actions/delete-an-appointment.md) | `DELETE /api/v1/appointments/:uuid` | [docs](https://developers.mihu.ai/api-reference/appointments/delete-an-appointment) |
| [Get a Specific Appointment](actions/get-a-specific-appointment.md) | `GET /api/v1/appointments/:uuid` | [docs](https://developers.mihu.ai/api-reference/appointments/get-a-specific-appointment) |
| [Get a Specific Appointment Request](actions/get-a-specific-appointment-request.md) | `GET /api/v1/appointment-requests/:uuid` | [docs](https://developers.mihu.ai/api-reference/appointment-requests/get-a-specific-appointment-request) |
| [Get a Specific Schedule](actions/get-a-specific-schedule.md) | `GET /api/v1/schedules/:uuid` | [docs](https://developers.mihu.ai/api-reference/schedules/get-a-specific-schedule) |
| [Get a Specific Task](actions/get-a-specific-task.md) | `GET /api/v1/tasks/:uuid` | [docs](https://developers.mihu.ai/api-reference/tasks/get-a-specific-task) |
| [Get All Appointments (Calendar)](actions/get-all-appointments-calendar.md) | `GET /api/v1/appointments` | [docs](https://developers.mihu.ai/api-reference/appointments/get-all-appointments-calendar) |
| [Get All Schedules](actions/get-all-schedules.md) | `GET /api/v1/schedules` | [docs](https://developers.mihu.ai/api-reference/schedules/get-all-schedules) |
| [Get Call Details by UUID](actions/get-call-details-by-uuid.md) | `GET /api/v1/calls/:uuid` | [docs](https://developers.mihu.ai/api-reference/call/get-call-details-by-uuid) |
| [Get Campaign Details](actions/get-campaign-details.md) | `GET /api/v1/campaigns/:uuid` | [docs](https://developers.mihu.ai/api-reference/campaigns/get-campaign-details) |
| [Get Contact Details](actions/get-contact-details.md) | `GET /api/v1/contacts/:uuid` | [docs](https://developers.mihu.ai/api-reference/contacts/get-contact-details) |
| [Get Full Transcript with Conversation Messages and Evaluations](actions/get-full-transcript-with-conversation-messages-and-evaluations.md) | `GET /api/v1/transcriptions/:uuid/transcript` | [docs](https://developers.mihu.ai/api-reference/transcriptions/get-full-transcript-with-conversation-messages-and-evaluations) |
| [Get List of Appointment Requests](actions/get-list-of-appointment-requests.md) | `GET /api/v1/appointment-requests` | [docs](https://developers.mihu.ai/api-reference/appointment-requests/get-list-of-appointment-requests) |
| [Get Paginated List of Calls](actions/get-paginated-list-of-calls.md) | `GET /api/v1/calls` | [docs](https://developers.mihu.ai/api-reference/call/get-paginated-list-of-calls) |
| [Get Paginated List of Campaigns](actions/get-paginated-list-of-campaigns.md) | `GET /api/v1/campaigns` | [docs](https://developers.mihu.ai/api-reference/campaigns/get-paginated-list-of-campaigns) |
| [Get Paginated List of Contacts](actions/get-paginated-list-of-contacts.md) | `GET /api/v1/contacts` | [docs](https://developers.mihu.ai/api-reference/contacts/get-paginated-list-of-contacts) |
| [Get Paginated List of Tasks](actions/get-paginated-list-of-tasks.md) | `GET /api/v1/tasks` | [docs](https://developers.mihu.ai/api-reference/tasks/get-paginated-list-of-tasks) |
| [Get Transcription by UUID](actions/get-transcription-by-uuid.md) | `GET /api/v1/transcriptions/:uuid` | [docs](https://developers.mihu.ai/api-reference/transcriptions/get-transcription-by-uuid) |
| [Initiate a New Call](actions/initiate-a-new-call.md) | `POST /api/v1/call` | [docs](https://developers.mihu.ai/api-reference/call/initiate-a-new-call) |
| [Queue a Task for Execution](actions/queue-a-task-for-execution.md) | `POST /api/v1/tasks/:uuid/queue` | [docs](https://developers.mihu.ai/api-reference/tasks/queue-a-task-for-execution) |
| [Remove Tag from Contact](actions/remove-tag-from-contact.md) | `POST /api/v1/contacts/:uuid/remove-tag` | [docs](https://developers.mihu.ai/api-reference/contacts/remove-tag-from-contact) |
| [Retry a Failed Task](actions/retry-a-failed-task.md) | `POST /api/v1/tasks/:uuid/retry` | [docs](https://developers.mihu.ai/api-reference/tasks/retry-a-failed-task) |
| [Update a Campaign](actions/update-a-campaign.md) | `PUT /api/v1/campaigns/:uuid` | [docs](https://developers.mihu.ai/api-reference/campaigns/update-a-campaign) |
| [Update a Contact](actions/update-a-contact.md) | `PUT /api/v1/contacts/:uuid` | [docs](https://developers.mihu.ai/api-reference/contacts/update-a-contact) |
| [Update a Schedule](actions/update-a-schedule.md) | `PUT /api/v1/schedules/:uuid` | [docs](https://developers.mihu.ai/api-reference/schedules/update-a-schedule) |
| [Update a Task](actions/update-a-task.md) | `PUT /api/v1/tasks/:uuid` | [docs](https://developers.mihu.ai/api-reference/tasks/update-a-task) |
| [Update an Appointment](actions/update-an-appointment.md) | `PUT /api/v1/appointments/:uuid` | [docs](https://developers.mihu.ai/api-reference/appointments/update-an-appointment) |
| [Update Appointment Status](actions/update-appointment-status.md) | `POST /api/v1/appointments/:uuid/status` | [docs](https://developers.mihu.ai/api-reference/appointments/update-appointment-status) |
