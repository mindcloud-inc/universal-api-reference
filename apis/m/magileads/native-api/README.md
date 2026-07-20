# Magileads: Native API Reference

A consolidated summary of Magileads's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://api.magileads.net
- **API base URL:** `https://app.api-magileads.net`

## Authentication

### API Key

Use a Magileads API key sent in the X-API-Key header for every request.

### Credentials

- **API Key:** `apiKey` · required · Your Magileads API key.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.magileads.net)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Blacklist](actions/create-blacklist.md) | `POST /blacklists` | [docs](https://api.magileads.net) |
| [Create Contact In List](actions/create-contact-in-list.md) | `POST /contact-lists/:contact_list_id/contact` | [docs](https://api.magileads.net) |
| [Create Contact List](actions/create-contact-list.md) | `POST /contact-lists` | [docs](https://api.magileads.net) |
| [Create PRM Custom Status](actions/create-prm-custom-status.md) | `POST /prm/status/custom` | [docs](https://api.magileads.net) |
| [Create PRM Nurturing](actions/create-prm-nurturing.md) | `POST /prm/nurturing` | [docs](https://api.magileads.net) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://api.magileads.net) |
| [Delete Blacklist](actions/delete-blacklist.md) | `DELETE /blacklists/:blacklist_id` | [docs](https://api.magileads.net) |
| [Delete Contact In List](actions/delete-contact-in-list.md) | `DELETE /contact-lists/:contact_list_id/contacts/:contact_id` | [docs](https://api.magileads.net) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /contact-lists/:contact_list_id` | [docs](https://api.magileads.net) |
| [Delete PRM Custom Status](actions/delete-prm-custom-status.md) | `DELETE /prm/status/custom/:status_id` | [docs](https://api.magileads.net) |
| [Delete PRM Nurturing](actions/delete-prm-nurturing.md) | `DELETE /prm/nurturing/:nurturing_id` | [docs](https://api.magileads.net) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tag_id` | [docs](https://api.magileads.net) |
| [Get Blacklist](actions/get-blacklist.md) | `GET /blacklists/:blacklist_id` | [docs](https://api.magileads.net) |
| [Get Contact](actions/get-contact.md) | `GET /contact-lists/:contact_list_id/contacts/:contact_id` | [docs](https://api.magileads.net) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contact-lists/:contact_list_id` | [docs](https://api.magileads.net) |
| [Get PRM Contact](actions/get-prm-contact.md) | `GET /prm/contact/:contact_id` | [docs](https://api.magileads.net) |
| [Get PRM Nurturing](actions/get-prm-nurturing.md) | `GET /prm/nurturing/:nurturing_id` | [docs](https://api.magileads.net) |
| [List Blacklists](actions/list-blacklists.md) | `GET /blacklists` | [docs](https://api.magileads.net) |
| [List Contact List Contacts](actions/list-contact-list-contacts.md) | `GET /contact-lists/:contact_list_id/contacts` | [docs](https://api.magileads.net) |
| [List Contact List Names](actions/list-contact-list-names.md) | `GET /contact-lists/names` | [docs](https://api.magileads.net) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contact-lists` | [docs](https://api.magileads.net) |
| [List PRM Contacts](actions/list-prm-contacts.md) | `GET /prm/contacts` | [docs](https://api.magileads.net) |
| [List PRM Custom Statuses](actions/list-prm-custom-statuses.md) | `GET /prm/status/custom` | [docs](https://api.magileads.net) |
| [List PRM Nurturings](actions/list-prm-nurturings.md) | `GET /prm/nurturings` | [docs](https://api.magileads.net) |
| [List PRM Statuses](actions/list-prm-statuses.md) | `GET /prm/status` | [docs](https://api.magileads.net) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://api.magileads.net) |
| [Search Contact List Contacts](actions/search-contact-list-contacts.md) | `POST /contact-lists/:contact_list_id/contacts/search` | [docs](https://api.magileads.net) |
| [Update Blacklist](actions/update-blacklist.md) | `PUT /blacklists/:blacklist_id` | [docs](https://api.magileads.net) |
| [Update Contact In List](actions/update-contact-in-list.md) | `PUT /contact-lists/:contact_list_id/contacts/:contact_id` | [docs](https://api.magileads.net) |
| [Update Contact List](actions/update-contact-list.md) | `PUT /contact-lists/:contact_list_id` | [docs](https://api.magileads.net) |
| [Update PRM Custom Status](actions/update-prm-custom-status.md) | `PUT /prm/status/custom/:status_id` | [docs](https://api.magileads.net) |
| [Update PRM Nurturing](actions/update-prm-nurturing.md) | `PUT /prm/nurturing/:nurturing_id` | [docs](https://api.magileads.net) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:tag_id` | [docs](https://api.magileads.net) |
