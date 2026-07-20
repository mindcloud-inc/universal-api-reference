# HappyFox: Native API Reference

A consolidated summary of HappyFox's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://support.happyfox.com/kb/article/360-api-for-happyfox/
- **API base URL:** `https://{accountDomain}/api/1.1/json`

## Authentication

### Basic

HTTP Basic authentication using HappyFox API key and auth code.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Account Domain:** `accountDomain` · required · Enter the full HappyFox account host, such as mindcloud.happyfox.com or mindcloud.happyfox.net. If you use a custom domain, enter that host instead.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.happyfox.com/kb/article/221-how-to-create-an-api-key-and-auth-code-in-happyfox/)

## API conventions

Response data is read from `data`. The total page count is read from `page_info.page_count`.

## Pagination

Use `size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Staff Private Note](actions/add-staff-private-note.md) | `POST /ticket/:ticket_number/staff_pvtnote/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Add Staff Update](actions/add-staff-update.md) | `POST /ticket/:ticket_number/staff_update/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Create Contact](actions/create-contact.md) | `POST /users/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Create Contact Group](actions/create-contact-group.md) | `POST /contact_groups/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Get Contact](actions/get-contact.md) | `GET /user/:user_id/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Get Ticket](actions/get-ticket.md) | `GET /ticket/:ticket_number/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [List Categories](actions/list-categories.md) | `GET /categories/` | [docs](https://support.happyfox.com/kb/article/360-api-for-happyfox/) |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | `GET /user_custom_fields/` | [docs](https://support.happyfox.com/kb/article/360-api-for-happyfox/) |
| [List Contact Groups](actions/list-contact-groups.md) | `GET /contact_groups/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [List Contacts](actions/list-contacts.md) | `GET /users/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [List Priorities](actions/list-priorities.md) | `GET /priorities/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [List Staff](actions/list-staff.md) | `GET /staff/` | [docs](https://support.happyfox.com/kb/article/360-api-for-happyfox/) |
| [List Statuses](actions/list-statuses.md) | `GET /statuses/` | [docs](https://support.happyfox.com/kb/article/360-api-for-happyfox/) |
| [List Ticket Custom Fields](actions/list-ticket-custom-fields.md) | `GET /ticket_custom_fields/` | [docs](https://support.happyfox.com/kb/article/360-api-for-happyfox/) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Move Ticket](actions/move-ticket.md) | `POST /ticket/:ticket_number/move/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Remove Contacts from Contact Group](actions/remove-contacts-from-contact-group.md) | `POST /contact_group/:contact_group_id/delete_contacts/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Update Contact](actions/update-contact.md) | `POST /user/:user_id/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Update Contact Group](actions/update-contact-group.md) | `POST /contact_group/:contact_group_id/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Update Contact Group Members](actions/update-contact-group-members.md) | `POST /contact_group/:contact_group_id/update_contacts/` | [docs](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/) |
| [Update Ticket Custom Fields](actions/update-ticket-custom-fields.md) | `POST /ticket/:ticket_number/update_custom_fields/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Update Ticket Properties](actions/update-ticket-properties.md) | `POST /ticket/:ticket_number/staff_update/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
| [Update Ticket Tags](actions/update-ticket-tags.md) | `POST /ticket/:ticket_number/update_tags/` | [docs](https://support.happyfox.com/kb/article/1039-tickets-endpoint/) |
