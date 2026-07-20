# HotspotSystem: Native API Reference

A consolidated summary of HotspotSystem's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.hotspotsystem.com/apidocs/api/reference/
- **API base URL:** `https://api.hotspotsystem.com/v2.0`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
sn-apikey: <apiKey>
```

[Official authentication documentation](https://www.hotspotsystem.com/apidocs/api/notes/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getcustomers) |
| [List Customers by Location](actions/list-customers-by-location.md) | `GET /locations/:locationId/customers` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getcustomersbylocationid) |
| [List Location Options](actions/list-location-options.md) | `GET /locations/options` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getlocationsasoptions) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getlocations) |
| [List MAC Transactions](actions/list-mac-transactions.md) | `GET /transactions/mac` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getmactransactions) |
| [List MAC Transactions by Location](actions/list-mac-transactions-by-location.md) | `GET /locations/:locationId/transactions/mac` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getmactransactionsbylocationid) |
| [List Paid Transactions](actions/list-paid-transactions.md) | `GET /transactions/paid` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getpaidtransactions) |
| [List Social Transactions](actions/list-social-transactions.md) | `GET /transactions/social` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getsocialtransactions) |
| [List Social Transactions by Location](actions/list-social-transactions-by-location.md) | `GET /locations/:locationId/transactions/social` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getsocialtransactionsbylocationid) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getsubscribers) |
| [List Subscribers by Location](actions/list-subscribers-by-location.md) | `GET /locations/:locationId/subscribers` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getsubscribersbylocationid) |
| [List Voucher Transactions](actions/list-voucher-transactions.md) | `GET /transactions/voucher` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getvouchertransactions) |
| [List Voucher Transactions by Location](actions/list-voucher-transactions-by-location.md) | `GET /locations/:locationId/transactions/voucher` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getvouchertransactionsbylocationid) |
| [Verify Credentials](actions/verify-credentials.md) | `GET /me` | [docs](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getme) |
