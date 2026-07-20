# EventGeek: Native API Reference

A consolidated summary of EventGeek's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.circa.co/
- **API base URL:** `https://app.circa.co/api/v1`

## Authentication

### API Key

Circa API key. Requests are sent with the key as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.circa.co/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Event](actions/add-contact-to-event.md) | `POST /events/:event_id/contacts` | [docs](https://docs.circa.co/) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://docs.circa.co/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.circa.co/) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://docs.circa.co/) |
| [Create Event Contacts Export](actions/create-event-contacts-export.md) | `POST /events/:event_id/contacts/exports` | [docs](https://docs.circa.co/) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/:company_id` | [docs](https://docs.circa.co/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://docs.circa.co/) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/:event_id` | [docs](https://docs.circa.co/) |
| [Delete Event Contacts Export](actions/delete-event-contacts-export.md) | `DELETE /events/:event_id/contacts/exports/:export_id` | [docs](https://docs.circa.co/) |
| [Get Company](actions/get-company.md) | `GET /companies/:company_id` | [docs](https://docs.circa.co/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://docs.circa.co/) |
| [Get Event](actions/get-event.md) | `GET /events/:event_id` | [docs](https://docs.circa.co/) |
| [Get Event Contact](actions/get-event-contact.md) | `GET /events/:event_id/contacts/:contact_id` | [docs](https://docs.circa.co/) |
| [Get Event Contacts Export](actions/get-event-contacts-export.md) | `GET /events/:event_id/contacts/exports/:export_id` | [docs](https://docs.circa.co/) |
| [Get Field](actions/get-field.md) | `GET /fields/:field_id` | [docs](https://docs.circa.co/) |
| [Get Team](actions/get-team.md) | `GET /teams/:team_id` | [docs](https://docs.circa.co/) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://docs.circa.co/) |
| [List Company Contacts](actions/list-company-contacts.md) | `GET /companies/:company_id/contacts` | [docs](https://docs.circa.co/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.circa.co/) |
| [List Event Contacts](actions/list-event-contacts.md) | `GET /events/:event_id/contacts` | [docs](https://docs.circa.co/) |
| [List Event Expenses](actions/list-event-expenses.md) | `GET /events/:event_id/expenses` | [docs](https://docs.circa.co/) |
| [List Event Staff](actions/list-event-staff.md) | `GET /events/:event_id/staff` | [docs](https://docs.circa.co/) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.circa.co/) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://docs.circa.co/) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.circa.co/) |
| [Remove Contact From Event](actions/remove-contact-from-event.md) | `DELETE /events/:event_id/contacts/:contact_id` | [docs](https://docs.circa.co/) |
| [Update Company](actions/update-company.md) | `PATCH /companies/:company_id` | [docs](https://docs.circa.co/) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:contact_id` | [docs](https://docs.circa.co/) |
| [Update Event](actions/update-event.md) | `PATCH /events/:event_id` | [docs](https://docs.circa.co/) |
| [Update Event Contact](actions/update-event-contact.md) | `PATCH /events/:event_id/contacts/:contact_id` | [docs](https://docs.circa.co/) |
