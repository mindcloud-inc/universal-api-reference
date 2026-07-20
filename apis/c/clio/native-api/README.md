# Clio Manage: Native API Reference

A consolidated summary of Clio Manage's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://docs.developers.clio.com/api-docs/clio-manage/
- **OpenAPI specification:** https://docs.developers.clio.com/openapi.json
- **API base URL:** `https://app.clio.com/api/v4`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.clio.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.clio.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `Contacts, Matters, Tasks, Notes, Activities, Calendar Entries`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.clio.com/oauth/token.

[Official authentication documentation](https://docs.developers.clio.com/api-docs/clio-manage/authorization/)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 200; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity Description](actions/create-activity-description.md) | `POST /activity_descriptions.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Descriptions/operation/ActivityDescription%23create) |
| [Create Activity Rate](actions/create-activity-rate.md) | `POST /activity_rates.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Rates/operation/ActivityRate%23create) |
| [Create Calendar Entry](actions/create-calendar-entry.md) | `POST /calendar_entries.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Calendar%20Entries/operation/CalendarEntry%23create) |
| [Create Matter](actions/create-matter.md) | `POST /matters.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matters/operation/Matter%23create) |
| [Create Matter Note](actions/create-matter-note.md) | `POST /notes.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Notes/operation/Note%23create) |
| [Create Person Contact](actions/create-person-contact.md) | `POST /contacts.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23create) |
| [Create Task](actions/create-task.md) | `POST /tasks.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Tasks/operation/Task%23create) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /activities.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activities/operation/Activity%23create) |
| [Get Activity](actions/get-activity.md) | `GET /activities/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activities/operation/Activity%23show) |
| [Get Activity Description](actions/get-activity-description.md) | `GET /activity_descriptions/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Descriptions/operation/ActivityDescription%23show) |
| [Get Activity Rate](actions/get-activity-rate.md) | `GET /activity_rates/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Rates/operation/ActivityRate%23show) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendars/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Calendars/operation/Calendar%23show) |
| [Get Calendar Entry](actions/get-calendar-entry.md) | `GET /calendar_entries/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Calendar%20Entries/operation/CalendarEntry%23show) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23show) |
| [Get Current User](actions/get-current-user.md) | `GET /users/who_am_i.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Users/operation/User%23who_am_i) |
| [Get Matter](actions/get-matter.md) | `GET /matters/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matters/operation/Matter%23show) |
| [Get Note](actions/get-note.md) | `GET /notes/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Notes/operation/Note%23show) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Tasks/operation/Task%23show) |
| [List Activities](actions/list-activities.md) | `GET /activities.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activities/operation/Activity%23index) |
| [List Activity Descriptions](actions/list-activity-descriptions.md) | `GET /activity_descriptions.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Descriptions/operation/ActivityDescription%23index) |
| [List Activity Rates](actions/list-activity-rates.md) | `GET /activity_rates.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Rates/operation/ActivityRate%23index) |
| [List Allocations](actions/list-allocations.md) | `GET /allocations.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Allocations/operation/Allocation%23index) |
| [List Calendar Entries](actions/list-calendar-entries.md) | `GET /calendar_entries.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Calendar%20Entries/operation/CalendarEntry%23index) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Calendars/operation/Calendar%23index) |
| [List Contact Email Addresses](actions/list-contact-email-addresses.md) | `GET /contacts/:contact_id/email_addresses.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Email%20Addresses/operation/EmailAddress%23index) |
| [List Contact Phone Numbers](actions/list-contact-phone-numbers.md) | `GET /contacts/:contact_id/phone_numbers.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Phone%20Numbers/operation/PhoneNumber%23index) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23index) |
| [List Matter Contacts](actions/list-matter-contacts.md) | `GET /matters/:matter_id/contacts.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matter%20Contacts/operation/MatterContacts%23index) |
| [List Matter Stages](actions/list-matter-stages.md) | `GET /matter_stages.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matter%20Stages/operation/MatterStage%23index) |
| [List Matters](actions/list-matters.md) | `GET /matters.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matters/operation/Matter%23index) |
| [List Notes](actions/list-notes.md) | `GET /notes.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Notes/operation/Note%23index) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Tasks/operation/Task%23index) |
| [Update Matter](actions/update-matter.md) | `PATCH /matters/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matters/operation/Matter%23update) |
| [Update Person Contact](actions/update-person-contact.md) | `PATCH /contacts/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23update) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id.json` | [docs](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Tasks/operation/Task%23update) |
