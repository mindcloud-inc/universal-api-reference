# Swoogo: Native API Reference

A consolidated summary of Swoogo's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://swoogo.readme.io/reference
- **API base URL:** `https://api.swoogo.com/api/v1`

## Authentication

### Consumer Key and Secret

### Credentials

- **Consumer Key:** `consumerKey` · required
- **Consumer Secret:** `consumerSecret` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://swoogo.readme.io/reference/post_oauth2-token)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. The total page count is read from `Meta.pageCount`. The current page number is read from `Meta.currentPage`.

## Pagination

Use `per-page` in the query string to set the page size (default 100; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Registrant](actions/get-registrant.md) | `GET /registrants/:registrant_id` | [docs](https://swoogo.readme.io/reference/getoneregistrant) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://swoogo.readme.io/reference/getallevents) |
| [List Registrants](actions/list-registrants.md) | `GET /registrants` | [docs](https://swoogo.readme.io/reference/getallregistrants) |
| [Update Registrant Contact ID](actions/update-registrant-contact-id.md) | `PUT /registrants/update/:registrant_id` | [docs](https://swoogo.readme.io/reference/updateregistrant) |
