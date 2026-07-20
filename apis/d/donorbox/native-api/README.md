# Donorbox: Native API Reference

A consolidated summary of Donorbox's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://github.com/donorbox/donorbox-api
- **API base URL:** `https://donorbox.org/api/v1`

## Authentication

### Basic Auth

Use your Donorbox account email as username and API key as password.

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

[Official authentication documentation](https://github.com/donorbox/donorbox-api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://github.com/donorbox/donorbox-api#campaigns) |
| [List Donations](actions/list-donations.md) | `GET /donations` | [docs](https://github.com/donorbox/donorbox-api#donations) |
| [List Donors](actions/list-donors.md) | `GET /donors` | [docs](https://github.com/donorbox/donorbox-api#donors) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://github.com/donorbox/donorbox-api#events) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://github.com/donorbox/donorbox-api#plans) |
| [List Purchases](actions/list-purchases.md) | `GET /purchases` | [docs](https://github.com/donorbox/donorbox-api#event-ticket-purchases) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://github.com/donorbox/donorbox-api#tickets) |
