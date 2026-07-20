# Sprintful: Native API Reference

A consolidated summary of Sprintful's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://support.sprintful.com/category/96-apis
- **API base URL:** `https://app.sprintful.com/api/v1`

## Authentication

### API Key

Connect Sprintful with an API key from Dashboard > Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.sprintful.com/article/129-sprintful-for-developers)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `offset` in the query string as the record offset.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | `GET /availability/:slug` | [docs](https://support.sprintful.com/article/129-sprintful-for-developers) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:id` | [docs](https://support.sprintful.com/article/129-sprintful-for-developers) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://support.sprintful.com/article/95-how-can-i-access-sprintful-via-apis) |
| [Get Page](actions/get-page.md) | `GET /pages/:slug` | [docs](https://support.sprintful.com/article/129-sprintful-for-developers) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://support.sprintful.com/article/129-sprintful-for-developers) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://support.sprintful.com/article/129-sprintful-for-developers) |
