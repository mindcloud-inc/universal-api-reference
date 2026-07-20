# Leadfox: Native API Reference

A consolidated summary of Leadfox's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf
- **API base URL:** `https://app.leadfox.co/service`

## Authentication

### API Key

Authenticate Leadfox requests with a key and secret.

### Credentials

- **API Key:** `apiKey` · required
- **Secret:** `secret` · required · Leadfox passphrase generated from the API management area.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contact/save/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
| [Delete Contact](actions/delete-contact.md) | `POST /contact/delete/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
| [Get Contact](actions/get-contact.md) | `POST /contact/get/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
| [Get Contact History](actions/get-contact-history.md) | `POST /contact/gethistory/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
| [List Contacts](actions/list-contacts.md) | `POST /contact/getlist/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
| [List Lists](actions/list-lists.md) | `POST /list/getlist/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
| [Update Contact](actions/update-contact.md) | `POST /contact/save/` | [docs](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf) |
