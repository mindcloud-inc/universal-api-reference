# Previsto: Native API Reference

A consolidated summary of Previsto's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.previsto.com/
- **API base URL:** `https://api.previsto.io`

## Authentication

### Basic Auth

Use the Previsto secret API key as the Basic Auth username and leave the password empty.

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

[Official authentication documentation](https://developer.previsto.com/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `size` in the query string to set the page size (default 20; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Assignment](actions/create-assignment.md) | `POST /assignments` | [docs](https://developer.previsto.com/assignments/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.previsto.com/contacts/) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://developer.previsto.com/organization/) |
| [Create Service Agreement](actions/create-service-agreement.md) | `POST /agreements` | [docs](https://developer.previsto.com/service-agreements/) |
| [Delete Assignment](actions/delete-assignment.md) | `DELETE /assignments/:id` | [docs](https://developer.previsto.com/assignments/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://developer.previsto.com/contacts/) |
| [Delete Service Agreement](actions/delete-service-agreement.md) | `DELETE /agreements/:id` | [docs](https://developer.previsto.com/service-agreements/) |
| [Get Current Account](actions/get-current-account.md) | `GET https://api.previsto.com/accounts/current` | [docs](https://developer.previsto.com/account/) |
| [List Assignments](actions/list-assignments.md) | `GET /assignments` | [docs](https://developer.previsto.com/assignments/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.previsto.com/contacts/) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developer.previsto.com/organization/) |
| [List Service Agreements](actions/list-service-agreements.md) | `GET /agreements` | [docs](https://developer.previsto.com/service-agreements/) |
| [Retrieve Assignment](actions/retrieve-assignment.md) | `GET /assignments/:id` | [docs](https://developer.previsto.com/assignments/) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/:id` | [docs](https://developer.previsto.com/contacts/) |
| [Retrieve Organization](actions/retrieve-organization.md) | `GET /organizations/:id` | [docs](https://developer.previsto.com/organization/) |
| [Retrieve Service Agreement](actions/retrieve-service-agreement.md) | `GET /agreements/:id` | [docs](https://developer.previsto.com/service-agreements/) |
| [Update Assignment](actions/update-assignment.md) | `PUT /assignments/:id` | [docs](https://developer.previsto.com/assignments/) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developer.previsto.com/contacts/) |
| [Update Organization](actions/update-organization.md) | `PUT /organizations/:id` | [docs](https://developer.previsto.com/organization/) |
| [Update Service Agreement](actions/update-service-agreement.md) | `PUT /agreements/:id` | [docs](https://developer.previsto.com/service-agreements/) |
