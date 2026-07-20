# Agile CRM: Native API Reference

A consolidated summary of Agile CRM's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://github.com/agilecrm/rest-api
- **API base URL:** `https://mindcloud.agilecrm.com/dev/api`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://github.com/agilecrm/rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 25). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `global_sort_key` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /contacts` | [docs](https://github.com/agilecrm/rest-api#21-creating-a-company) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://github.com/agilecrm/rest-api#13-creating-a-contact) |
| [Create Deal](actions/create-deal.md) | `POST /opportunity` | [docs](https://github.com/agilecrm/rest-api#33-create-deal) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://github.com/agilecrm/rest-api#41-create-a-note-and-relate-that-to-contacts) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://github.com/agilecrm/rest-api#54-create-a-task) |
| [Delete Company](actions/delete-company.md) | `DELETE /contacts/{{companyId}}` | [docs](https://github.com/agilecrm/rest-api#25-delete-single-company) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{contactId}}` | [docs](https://github.com/agilecrm/rest-api#110-delete-single-contact) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /opportunity/:dealId` | [docs](https://github.com/agilecrm/rest-api#36-delete-deal) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://github.com/agilecrm/rest-api#12-get-contact-by-id) |
| [List Companies](actions/list-companies.md) | `POST /contacts/companies/list` | [docs](https://github.com/agilecrm/rest-api#23-get-list-of-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://github.com/agilecrm/rest-api#11-listing-contacts-) |
| [List Deals](actions/list-deals.md) | `GET /opportunity` | [docs](https://github.com/agilecrm/rest-api#31-listing-deals) |
| [Search Contacts and Companies](actions/search-contacts-and-companies.md) | `GET /search` | [docs](https://github.com/agilecrm/rest-api#111-search-contactscompanies) |
| [Update Company](actions/update-company.md) | `PUT /contacts/edit-properties` | [docs](https://github.com/agilecrm/rest-api#22-updating-a-company) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/edit-properties` | [docs](https://github.com/agilecrm/rest-api#14-update-properties-of-a-contact-by-id-partial-update) |
| [Update Contact Tags](actions/update-contact-tags.md) | `PUT /contacts/edit/tags` | [docs](https://github.com/agilecrm/rest-api#17-update-tags-value-by-id) |
| [Update Deal](actions/update-deal.md) | `PUT /opportunity/partial-update` | [docs](https://github.com/agilecrm/rest-api#34-update-deal-partial-update) |
