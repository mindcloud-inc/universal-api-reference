# JustCall: Native API Reference

A consolidated summary of JustCall's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.justcall.io/reference
- **API base URL:** `https://api.justcall.io`

## Authentication

### API Key + Secret

Use your JustCall API key and API secret.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.justcall.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Add Contacts to Blacklist](actions/bulk-add-contacts-to-blacklist.md) | `POST /v2.1/contacts/bulk-add/blacklist` | [docs](https://developer.justcall.io/reference/bulk_add_contacts_to_blacklist_v21) |
| [Check Reply](actions/check-reply.md) | `POST /v2.1/texts/checkreply` | [docs](https://developer.justcall.io/reference/texts_checkreply_v21) |
| [Create Contact](actions/create-contact.md) | `POST /v2.1/contacts` | [docs](https://developer.justcall.io/reference/create_contact_v21) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v2.1/contacts` | [docs](https://developer.justcall.io/reference/delete_contact_v21) |
| [Download Call Recording](actions/download-call-recording.md) | `GET /v2.1/calls/:id/recording/download` | [docs](https://developer.justcall.io/reference/call_recording_download_v21) |
| [Get a Call](actions/get-a-call.md) | `GET /v2.1/calls/:id` | [docs](https://developer.justcall.io/reference/call_get_v21) |
| [Get a Contact](actions/get-a-contact.md) | `GET /v2.1/contacts/:id` | [docs](https://developer.justcall.io/reference/contact_get_v21) |
| [Get a Phone Number](actions/get-a-phone-number.md) | `GET /v2.1/phone-numbers/:id` | [docs](https://developer.justcall.io/reference/phone_number_get_v21) |
| [Get a Text](actions/get-a-text.md) | `GET /v2.1/texts/:id` | [docs](https://developer.justcall.io/reference/texts_get_v21) |
| [Get a Thread](actions/get-a-thread.md) | `GET /v2.1/texts/threads/:thread_id` | [docs](https://developer.justcall.io/reference/texts_threads_get_v21) |
| [Get a User](actions/get-a-user.md) | `GET /v2.1/users/:id` | [docs](https://developer.justcall.io/reference/users_get_v21) |
| [Get Call Journey](actions/get-call-journey.md) | `GET /v2.1/calls/:id/journey` | [docs](https://developer.justcall.io/reference/call_get_journey_v21) |
| [List All Calls](actions/list-all-calls.md) | `GET /v2.1/calls` | [docs](https://developer.justcall.io/reference/call_list_v21) |
| [List All Contacts](actions/list-all-contacts.md) | `GET /v2.1/contacts` | [docs](https://developer.justcall.io/reference/contacts_list_v21) |
| [List All Phone Numbers](actions/list-all-phone-numbers.md) | `GET /v2.1/phone-numbers` | [docs](https://developer.justcall.io/reference/phone_number_list_v21) |
| [List All Texts](actions/list-all-texts.md) | `GET /v2.1/texts` | [docs](https://developer.justcall.io/reference/texts_list_v21) |
| [List All Threads](actions/list-all-threads.md) | `GET /v2.1/texts/threads` | [docs](https://developer.justcall.io/reference/texts_threads_list_v21) |
| [List All Users](actions/list-all-users.md) | `GET /v2.1/users` | [docs](https://developer.justcall.io/reference/users_list_v21) |
| [List Blacklisted Contacts](actions/list-blacklisted-contacts.md) | `GET /v2.1/contacts/blacklist` | [docs](https://developer.justcall.io/reference/list_blacklist_contacts_v21) |
| [Send SMS/MMS](actions/send-sms-mms.md) | `POST /v2.1/texts/new` | [docs](https://developer.justcall.io/reference/texts_new_v21) |
| [Update a Call](actions/update-a-call.md) | `PUT /v2.1/calls/:id` | [docs](https://developer.justcall.io/reference/call_update_v21) |
| [Update Contact](actions/update-contact.md) | `PUT /v2.1/contacts` | [docs](https://developer.justcall.io/reference/update_contact_v21) |
| [Update Contact Status](actions/update-contact-status.md) | `PUT /v2.1/contacts/status` | [docs](https://developer.justcall.io/reference/update_contact_status_v21) |
| [Update User Availability](actions/update-user-availability.md) | `PUT /v2.1/users/availability` | [docs](https://developer.justcall.io/reference/update_user_availability_v21) |
