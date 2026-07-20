# HirePOS: Native API Reference

A consolidated summary of HirePOS's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.hirepos.com/en/categories/524033-hirepos-api
- **API base URL:** `https://api.hirepos.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Auth Secret:** `authSecret` · required · Your HirePOS API secret.

Send these headers with each API request:

```http
AuthKey: <apiKey>
AuthSecret: <authSecret>
```

[Official authentication documentation](https://docs.hirepos.com/en/articles/2314817)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `GET /Authenticate` | [docs](https://docs.hirepos.com/en/articles/2314817) |
| [Create Customer](actions/create-customer.md) | `POST /Customers` | [docs](https://docs.hirepos.com/en/articles/2314561) |
| [Create Lead](actions/create-lead.md) | `POST /Leads` | [docs](https://docs.hirepos.com/en/articles/3907009) |
| [Create Website Booking](actions/create-website-booking.md) | `POST /WebsiteBookings` | [docs](https://docs.hirepos.com/en/articles/2314369) |
| [Get Availability](actions/get-availability.md) | `GET /Availability` | [docs](https://docs.hirepos.com/en/articles/2314625) |
| [Get Delivery Pickup Status](actions/get-delivery-pickup-status.md) | `GET /DeliveryPickupStatus` | [docs](https://docs.hirepos.com/en/articles/9534913) |
| [Get Last Website Order](actions/get-last-website-order.md) | `GET /LastWebsiteOrder` | [docs](https://docs.hirepos.com/en/articles/2314881) |
| [Get Package](actions/get-package.md) | `GET /Packages` | [docs](https://docs.hirepos.com/en/articles/3084161) |
| [Get Website Booking](actions/get-website-booking.md) | `GET /WebsiteBookings` | [docs](https://docs.hirepos.com/en/articles/2314369) |
| [List Dispatched Today](actions/list-dispatched-today.md) | `GET /DispatchedToday` | [docs](https://docs.hirepos.com/en/articles/2314689) |
| [List Items](actions/list-items.md) | `GET /Items` | [docs](https://docs.hirepos.com/en/articles/3084097) |
| [List Returned Today](actions/list-returned-today.md) | `GET /ReturnedToday` | [docs](https://docs.hirepos.com/en/articles/2314753) |
| [List Sales Stock Levels](actions/list-sales-stock-levels.md) | `GET /API/SalesStockLevels` | [docs](https://docs.hirepos.com/en/articles/8667457) |
