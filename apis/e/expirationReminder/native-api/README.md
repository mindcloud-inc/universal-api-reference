# Expiration Reminder: Native API Reference

A consolidated summary of Expiration Reminder's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.expirationreminder.com/
- **API base URL:** `https://api.expirationreminder.net`

## Authentication

### API Key

Connect with an Expiration Reminder API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.expirationreminder.com/docs/authentication)

## API conventions

The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `sortDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File to Expiration Item](actions/add-file-to-expiration-item.md) | `POST /v1/expirationitems/:id/attachment` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-add-a-file-to-an-expiration-item) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://developers.expirationreminder.com/api-reference/contacts-create-a-contact) |
| [Create Contact Type](actions/create-contact-type.md) | `POST /v1/contacttypes` | [docs](https://developers.expirationreminder.com/api-reference/contact-types-create-a-contact-type) |
| [Create Document Type](actions/create-document-type.md) | `POST /v1/categories` | [docs](https://developers.expirationreminder.com/api-reference/document-types-create-a-document-type) |
| [Create Expiration Item](actions/create-expiration-item.md) | `POST /v1/expirationitems` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-create-an-expiration-item) |
| [Create Location](actions/create-location.md) | `POST /v1/locations` | [docs](https://developers.expirationreminder.com/api-reference/locations-create-a-location) |
| [Create Workspace](actions/create-workspace.md) | `POST /v1/teams` | [docs](https://developers.expirationreminder.com/api-reference/workspaces-create-a-workspace) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/:id` | [docs](https://developers.expirationreminder.com/api-reference/contacts-delete-a-contact) |
| [Delete Contact Type](actions/delete-contact-type.md) | `DELETE /v1/contacttypes/:id` | [docs](https://developers.expirationreminder.com/api-reference/contact-types-delete-a-contact-type) |
| [Delete Document Type](actions/delete-document-type.md) | `DELETE /v1/categories/:id` | [docs](https://developers.expirationreminder.com/api-reference/document-types-delete-a-document-type) |
| [Delete Expiration Item](actions/delete-expiration-item.md) | `DELETE /v1/expirationitems/:id` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-delete-an-expiration-item) |
| [Delete Location](actions/delete-location.md) | `DELETE /v1/locations/:id` | [docs](https://developers.expirationreminder.com/api-reference/locations-delete-a-location) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /v1/teams/:id` | [docs](https://developers.expirationreminder.com/api-reference/workspaces-delete-a-workspace) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/:id` | [docs](https://developers.expirationreminder.com/api-reference/contacts-get-a-contact) |
| [Get Contact Type](actions/get-contact-type.md) | `GET /v1/contacttypes/:id` | [docs](https://developers.expirationreminder.com/api-reference/contact-types-get-a-contact-type) |
| [Get Document Type](actions/get-document-type.md) | `GET /v1/categories/:id` | [docs](https://developers.expirationreminder.com/api-reference/document-types-get-a-document-type) |
| [Get Event Log](actions/get-event-log.md) | `GET /v1/eventlogs/:id` | [docs](https://developers.expirationreminder.com/api-reference/event-log-get-an-event-log) |
| [Get Expiration Item](actions/get-expiration-item.md) | `GET /v1/expirationitems/:id` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-get-an-expiration-item) |
| [Get File Detail](actions/get-file-detail.md) | `GET /v1/attachments/expirationitem/:id` | [docs](https://developers.expirationreminder.com/api-reference/files-get-a-file%27s-detail) |
| [Get Location](actions/get-location.md) | `GET /v1/locations/:id` | [docs](https://developers.expirationreminder.com/api-reference/locations-get-a-location) |
| [Get User](actions/get-user.md) | `GET /v1/users/:id` | [docs](https://developers.expirationreminder.com/api-reference/users-get-a-user) |
| [Get Workspace](actions/get-workspace.md) | `GET /v1/teams/:id` | [docs](https://developers.expirationreminder.com/api-reference/workspaces-get-a-workspace) |
| [List Contact Types](actions/list-contact-types.md) | `GET /v1/contacttypes` | [docs](https://developers.expirationreminder.com/api-reference/contact-types-get-all-contact-types) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://developers.expirationreminder.com/api-reference/contacts-get-all-contacts) |
| [List Document Types](actions/list-document-types.md) | `GET /v1/categories` | [docs](https://developers.expirationreminder.com/api-reference/document-types-get-all-document-types) |
| [List Event Logs](actions/list-event-logs.md) | `GET /v1/eventlogs` | [docs](https://developers.expirationreminder.com/api-reference/event-log-get-all-event-logs) |
| [List Expiration Items](actions/list-expiration-items.md) | `GET /v1/expirationitems` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-get-all-expiration-items) |
| [List Expiration Items for Contact](actions/list-expiration-items-for-contact.md) | `GET /v1/expirationitems/contact/:id` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-get-all-expiration-items-for-a-contact) |
| [List Files Related to Expiration Items](actions/list-files-related-to-expiration-items.md) | `GET /v1/attachments/expirationitem` | [docs](https://developers.expirationreminder.com/api-reference/files-get-all-files-related-to-expiration-items) |
| [List Locations](actions/list-locations.md) | `GET /v1/locations` | [docs](https://developers.expirationreminder.com/api-reference/locations-get-all-locations) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/teams` | [docs](https://developers.expirationreminder.com/api-reference/workspaces-get-all-workspaces) |
| [Renew an expiration item](actions/renew-an-expiration-item-post.md) | `POST /v1/expirationitems/:id/renew` |  |
| [Renew Expiration Item](actions/renew-expiration-item.md) | `PUT /v1/expirationitems/:id/renew` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-renew-an-expiration-item) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contacts/:id` | [docs](https://developers.expirationreminder.com/api-reference/contacts-update-a-contact) |
| [Update Contact Type](actions/update-contact-type.md) | `PUT /v1/contacttypes/:id` | [docs](https://developers.expirationreminder.com/api-reference/contact-types-update-a-contact-type) |
| [Update Contacts in Expiration Item](actions/update-contacts-in-expiration-item.md) | `POST /v1/expirationitems/:id/contacts` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-update-contacts-in-an-expiration-item) |
| [Update Document Type](actions/update-document-type.md) | `PUT /v1/categories/:id` | [docs](https://developers.expirationreminder.com/api-reference/document-types-update-a-document-type) |
| [Update Expiration Item](actions/update-expiration-item.md) | `PUT /v1/expirationitems/:id` | [docs](https://developers.expirationreminder.com/api-reference/expiration-items-update-an-expiration-item) |
| [Update Location](actions/update-location.md) | `PUT /v1/locations/:id` | [docs](https://developers.expirationreminder.com/api-reference/locations-update-a-location) |
| [Update Workspace](actions/update-workspace.md) | `PUT /v1/teams/:id` | [docs](https://developers.expirationreminder.com/api-reference/workspaces-update-a-workspace) |
