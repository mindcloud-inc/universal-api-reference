# Channels: Native API Reference

A consolidated summary of Channels's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.channels.app/
- **API base URL:** `https://api.channels.app`

## Authentication

### API Key

Authenticate Channels API requests with the x-api-token header and required Account header.

### Credentials

- **API Key:** `apiKey` · required
- **Account:** `account` · required · Channels account identifier sent in the Account header.

Send these headers with each API request:

```http
Account: <account>
x-api-token: <apiKey>
```

[Official authentication documentation](https://developers.channels.app/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Alternative MSISDN](actions/add-contact-alternative-msisdn.md) | `POST /api/v1/contacts/{contactId}/alternative-msisdns` | [docs](https://developers.channels.app/) |
| [Add Contact Note](actions/add-contact-note.md) | `POST /api/v1/contacts/{contactId}/note` | [docs](https://developers.channels.app/) |
| [Add Or Update Contact Details](actions/add-or-update-contact-details.md) | `POST /api/v1/contacts/{contactId}/details` | [docs](https://developers.channels.app/) |
| [Block MSISDN](actions/block-msisdn.md) | `POST /api/v1/dnclist/block` | [docs](https://developers.channels.app/) |
| [Check User Exists](actions/check-user-exists.md) | `GET /api/v1/users/exists` | [docs](https://developers.channels.app/) |
| [Create Public Recording Link](actions/create-public-recording-link.md) | `POST /api/v1/recordings` | [docs](https://developers.channels.app/) |
| [Create Recordings Archive Link](actions/create-recordings-archive-link.md) | `POST /api/v1/archive` | [docs](https://developers.channels.app/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/v1/contacts/{contactId}` | [docs](https://developers.channels.app/) |
| [Delete Contact Alternative MSISDN](actions/delete-contact-alternative-msisdn.md) | `DELETE /api/v1/contacts/{contactId}/alternative-msisdns/{msisdnId}` | [docs](https://developers.channels.app/) |
| [Delete Public Recording Link](actions/delete-public-recording-link.md) | `DELETE /api/v1/recordings/{token}` | [docs](https://developers.channels.app/) |
| [Disable User](actions/disable-user.md) | `PUT /api/v1/users/{userId}/disable` | [docs](https://developers.channels.app/) |
| [Edit Contact Details](actions/edit-contact-details.md) | `PUT /api/v1/contacts/{contactId}/details` | [docs](https://developers.channels.app/) |
| [Enable User](actions/enable-user.md) | `PUT /api/v1/users/{userId}/enable` | [docs](https://developers.channels.app/) |
| [Get Call](actions/get-call.md) | `GET /api/v1/calls/{id}` | [docs](https://developers.channels.app/) |
| [Get Contact](actions/get-contact.md) | `GET /api/v1/contacts/{contactId}` | [docs](https://developers.channels.app/) |
| [Get Contact Details](actions/get-contact-details.md) | `GET /api/v1/contacts/{contactId}/details` | [docs](https://developers.channels.app/) |
| [Get Contact History](actions/get-contact-history.md) | `GET /api/v1/contacts/{contactId}/history` | [docs](https://developers.channels.app/) |
| [Get Number Do Not Call History](actions/get-number-do-not-call-history.md) | `GET /api/v1/dnclist/{msisdn}` | [docs](https://developers.channels.app/) |
| [Get User Stats](actions/get-user-stats.md) | `GET /api/v1/users/stats` | [docs](https://developers.channels.app/) |
| [Import Contact](actions/import-contact.md) | `POST /api/v1/contacts` | [docs](https://developers.channels.app/) |
| [List Calls](actions/list-calls.md) | `GET /api/v1/calls` | [docs](https://developers.channels.app/) |
| [List Contact Alternative MSISDNs](actions/list-contact-alternative-msisd-ns.md) | `GET /api/v1/contacts/{contactId}/alternative-msisdns` | [docs](https://developers.channels.app/) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v1/contacts` | [docs](https://developers.channels.app/) |
| [List Do Not Call History](actions/list-do-not-call-history.md) | `GET /api/v1/dnclist` | [docs](https://developers.channels.app/) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /api/v1/msisdns` | [docs](https://developers.channels.app/) |
| [List Public Recording Links](actions/list-public-recording-links.md) | `GET /api/v1/recordings` | [docs](https://developers.channels.app/) |
| [List Users](actions/list-users.md) | `GET /api/v1/users` | [docs](https://developers.channels.app/) |
| [Set Inbound Call Forwarding](actions/set-inbound-call-forwarding.md) | `POST /api/v1/inbound/configuration/numbers/{msisdnId}/forward` | [docs](https://developers.channels.app/) |
| [Unblock MSISDN](actions/unblock-msisdn.md) | `POST /api/v1/dnclist/unblock` | [docs](https://developers.channels.app/) |
| [Update Contact](actions/update-contact.md) | `POST /api/v1/contacts/{contactId}` | [docs](https://developers.channels.app/) |
