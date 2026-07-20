# Corsizio: Native API Reference

A consolidated summary of Corsizio's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://help.corsizio.com/category/28-developer-api
- **API base URL:** `https://api.corsizio.com/v1`

## Authentication

### API Secret Key

Authenticate with a Corsizio API Secret Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.corsizio.com/article/37-api-endpoint-authentication)

## API conventions

Responses from this API use JSON. The current page number is read from `paging.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://help.corsizio.com/article/38-api-get-account-details) |
| [Get Attendee Details](actions/get-attendee-details.md) | `GET /attendees/:id` | [docs](https://help.corsizio.com/article/44-api-get-attendee-details) |
| [Get Event Details](actions/get-event-details.md) | `GET /events/:id` | [docs](https://help.corsizio.com/article/41-api-get-event-details) |
| [List Attendees](actions/list-attendees.md) | `GET /attendees` | [docs](https://help.corsizio.com/article/43-api-get-attendees-list) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://help.corsizio.com/article/39-api-get-events-list) |
