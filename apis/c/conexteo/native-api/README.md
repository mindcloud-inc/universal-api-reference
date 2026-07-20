# Conexteo: Native API Reference

A consolidated summary of Conexteo's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://developers.conexteo.com
- **API base URL:** `https://api.conexteo.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · Your Conexteo App ID from Mon Compte > Api / Webhook.

Send these headers with each API request:

```http
X-APP-ID: <appId>
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developers.conexteo.com/cr%C3%A9dits-24126498e0)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.totalPages`. The current page number is read from `meta.currentPage`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contacts](actions/add-contacts.md) | `POST /contacts` | [docs](https://developers.conexteo.com/ajouter-undes-contacts-24126523e0) |
| [Create Contact List](actions/create-contact-list.md) | `POST /contactlists` | [docs](https://developers.conexteo.com/cr%C3%A9er-une-liste-de-contacts-24126516e0) |
| [Create Manual Stop](actions/create-manual-stop.md) | `POST /stops` | [docs](https://developers.conexteo.com/ajout-dun-stop-manuel-24126513e0) |
| [Create Model](actions/create-model.md) | `POST /models` | [docs](https://developers.conexteo.com/cr%C3%A9ation-du-mod%C3%A8le-24126529e0) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://developers.conexteo.com/suppression-dun-contact-24126527e0) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /contactlists/:id` | [docs](https://developers.conexteo.com/suppression-dune-liste-de-contacts-24126520e0) |
| [Delete Stop](actions/delete-stop.md) | `DELETE /stops/:id` | [docs](https://developers.conexteo.com/suppression-dun-stop-24126515e0) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contactlists/:id` | [docs](https://developers.conexteo.com/d%C3%A9tail-dune-liste-de-contacts-24126519e0) |
| [Get Credits](actions/get-credits.md) | `GET /users/credits` | [docs](https://developers.conexteo.com/cr%C3%A9dits-24126498e0) |
| [Get Model](actions/get-model.md) | `GET /models/:id` | [docs](https://developers.conexteo.com/d%C3%A9tail-du-mod%C3%A8le-24126532e0) |
| [List All Message Replies](actions/list-all-message-replies.md) | `GET /messages/replies/extract` | [docs](https://developers.conexteo.com/r%C3%A9ponses-complet-24126506e0) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contactlists` | [docs](https://developers.conexteo.com/liste-des-listes-de-contacts-24126517e0) |
| [List Contacts In Contact List](actions/list-contacts-in-contact-list.md) | `GET /contactlists/:id/contacts` | [docs](https://developers.conexteo.com/contacts-dune-liste-de-contacts-pagination-24126521e0) |
| [List Message History](actions/list-message-history.md) | `GET /messages` | [docs](https://developers.conexteo.com/historique-des-messages-24126499e0) |
| [List Message Replies](actions/list-message-replies.md) | `GET /messages/replies` | [docs](https://developers.conexteo.com/r%C3%A9ponses-pagination-24126505e0) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://developers.conexteo.com/liste-des-mod%C3%A8les-24126530e0) |
| [List RCS Models](actions/list-rcs-models.md) | `GET /models/rcs` | [docs](https://developers.conexteo.com/liste-des-mod%C3%A8les-rcs-24126535e0) |
| [List Stops](actions/list-stops.md) | `GET /stops/all` | [docs](https://developers.conexteo.com/liste-des-stops-24126512e0) |
| [Send Dynamic SMS](actions/send-dynamic-sms.md) | `POST /messages/sms/dynamic` | [docs](https://developers.conexteo.com/envoi-dynamique-24126509e0) |
| [Send Manual SMS](actions/send-manual-sms.md) | `POST /messages/sms` | [docs](https://developers.conexteo.com/envoi-manuel-24126508e0) |
| [Send SMS To Contact Lists](actions/send-sms-to-contact-lists.md) | `POST /messages/sms/contactlist` | [docs](https://developers.conexteo.com/envoi-liste-de-contacts-24126510e0) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developers.conexteo.com/mise-%C3%A0-jour-dun-contact-24126525e0) |
| [Update Contact List](actions/update-contact-list.md) | `PUT /contactlists/:id` | [docs](https://developers.conexteo.com/mise-%C3%A0-jour-dune-liste-de-contacts-24126518e0) |
