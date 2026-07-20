# VoilaNorbert: Native API Reference

A consolidated summary of VoilaNorbert's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://api.voilanorbert.com/2018-01-08/
- **API base URL:** `https://api.voilanorbert.com/2018-01-08`

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

[Official authentication documentation](https://api.voilanorbert.com/2018-01-08/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `result`. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_by` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create List](actions/create-list.md) | `POST /lists/` | [docs](https://api.voilanorbert.com/2018-01-08/#lists-lists-post) |
| [Get Account](actions/get-account.md) | `GET /account/` | [docs](https://api.voilanorbert.com/2018-01-08/#account-get) |
| [Get Bulk File](actions/get-bulk-file.md) | `GET /massives/:id` | [docs](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-item-operations-get) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api.voilanorbert.com/2018-01-08/#contacts-get-1) |
| [Get List](actions/get-list.md) | `GET /lists/:id` | [docs](https://api.voilanorbert.com/2018-01-08/#lists-list-items-get) |
| [Get Organization](actions/get-organization.md) | `GET /organization/` | [docs](https://api.voilanorbert.com/2018-01-08/#organization-get) |
| [Get Organization Credits](actions/get-organization-credits.md) | `GET /organization/credits` | [docs](https://api.voilanorbert.com/2018-01-08/#credits-get) |
| [List Bulk Files](actions/list-bulk-files.md) | `GET /massives/` | [docs](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-operations-get) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://api.voilanorbert.com/2018-01-08/#contacts-get) |
| [List Lists](actions/list-lists.md) | `GET /lists/` | [docs](https://api.voilanorbert.com/2018-01-08/#lists-lists-get) |
| [Pause Bulk File](actions/pause-bulk-file.md) | `POST /massives/:id/pause` | [docs](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-item-operations-post-1) |
| [Remove Bulk File](actions/remove-bulk-file.md) | `DELETE /massives/:id` | [docs](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-item-operations-delete) |
| [Resume Bulk File](actions/resume-bulk-file.md) | `POST /massives/:id/resume` | [docs](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-item-operations-post) |
| [Search By Domain](actions/search-by-domain.md) | `POST /search/domain` | [docs](https://api.voilanorbert.com/2018-01-08/#search-endpoint-post-1) |
| [Search By Name](actions/search-by-name.md) | `POST /search/name` | [docs](https://api.voilanorbert.com/2018-01-08/#search-endpoint-post) |
| [Submit Bulk File](actions/submit-bulk-file.md) | `POST /massives/` | [docs](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-operations-post) |
| [Update List](actions/update-list.md) | `PUT /lists/:id` | [docs](https://api.voilanorbert.com/2018-01-08/#lists-list-items-put) |
