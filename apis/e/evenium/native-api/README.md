# Evenium: Native API Reference

A consolidated summary of Evenium's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://static.evenium.com/api-docs/organizer/index-json.html
- **API base URL:** `https://evenium.com/api/1`

## Authentication

### API Key

Use an Evenium API access token. MindCloud sends the token in the X-Evenium-Token header.

### Credentials

- **API Key:** `apiKey` · required · Paste your Evenium API key. MindCloud sends it in the X-Evenium-Token header.

Send these headers with each API request:

```http
X-Evenium-Token: <apiKey>
```

[Official authentication documentation](https://static.evenium.com/api-docs/organizer/index-json.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `events`.

## Pagination

Use `maxResults` in the query string to set the page size (default 100). Use `firstResult` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_create_contact) |
| [Create Event](actions/create-event.md) | `POST https://evenium.com/api/2/member/events` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_create_events) |
| [Create Guest](actions/create-guest.md) | `POST /events/:eventId/guests` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_create_guest) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_remove_contact) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_contact) |
| [Get Contact by Custom ID](actions/get-contact-by-custom-id.md) | `GET /contacts/customId/:customId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_contact_by_custom_id) |
| [Get Event](actions/get-event.md) | `GET /events/:eventId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_event) |
| [Get Event Part](actions/get-event-part.md) | `GET /events/:eventId/eventParts/:eventPartId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_event_part) |
| [Get Guest](actions/get-guest.md) | `GET /events/:eventId/guests/:contactId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest) |
| [Get Guest Post Status](actions/get-guest-post-status.md) | `GET /events/:eventId/guests/:contactId/postStatus` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest_post_status) |
| [Get Guest Status](actions/get-guest-status.md) | `GET /events/:eventId/guests/:contactId/status` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest_status) |
| [Import Contacts](actions/import-contacts.md) | `PUT /contacts` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_import_contacts) |
| [Import Guests](actions/import-guests.md) | `PUT /events/:eventId/guests` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_import_guests) |
| [List Contact Events](actions/list-contact-events.md) | `GET /contacts/:contactId/events` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_contacts_events) |
| [List Contact Events by Custom ID](actions/list-contact-events-by-custom-id.md) | `GET /contacts/customId/:customId/events` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_contacts_events_by_custom_id) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_contacts) |
| [List Event Part Registrations](actions/list-event-part-registrations.md) | `GET /events/:eventId/eventParts/:eventPartId/registrations` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_registrations_by_event_part) |
| [List Event Parts](actions/list-event-parts.md) | `GET /events/:eventId/eventParts` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_event_parts) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_events) |
| [List Guest Accommodations](actions/list-guest-accommodations.md) | `GET /events/:eventId/guests/:contactId/accommodations` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest_accommodations) |
| [List Guests](actions/list-guests.md) | `GET /events/:eventId/guests` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_guests) |
| [List Hotels](actions/list-hotels.md) | `GET /events/:eventId/hotels` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_get_hotels) |
| [Log In](actions/log-in.md) | `POST /loginOAuth` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_log_in) |
| [Log Out](actions/log-out.md) | `GET /logout/` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_log_out) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contactId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_update_contact) |
| [Update Contact by Custom ID](actions/update-contact-by-custom-id.md) | `PUT /contacts/customId/:customId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_update_contact_by_custom_id) |
| [Update Guest](actions/update-guest.md) | `PUT /events/:eventId/guests/:contactId` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest) |
| [Update Guest Photo](actions/update-guest-photo.md) | `PUT /events/:eventId/guests/:contactId/photo` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest_photo) |
| [Update Guest Post Status](actions/update-guest-post-status.md) | `PUT /events/:eventId/guests/:contactId/postStatus` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest_post_status) |
| [Update Guest Status](actions/update-guest-status.md) | `PUT /events/:eventId/guests/:contactId/status` | [docs](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest_status) |
