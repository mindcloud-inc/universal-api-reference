# Cituro: Native API Reference

A consolidated summary of Cituro's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://www.cituro.com/help/developers-corner/schnittstellen
- **API base URL:** `https://app.cituro.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://www.cituro.com/help/developers-corner/schnittstellen/api-key-erstellen)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Appointment](actions/get-appointment.md) | `GET /appointments/:appointmentId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Coupon](actions/get-coupon.md) | `GET /coupons/:couponId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Discount](actions/get-discount.md) | `GET /discounts/:discountId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Location](actions/get-location.md) | `GET /locations/:locationId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Ratings Summary](actions/get-ratings-summary.md) | `GET /ratings/:accountNumber/summary` | [docs](https://www.cituro.com/help/bewertungen-auf-webseite-einbinden) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:resourceId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Get Service](actions/get-service.md) | `GET /services/:serviceId` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Appointments](actions/list-appointments.md) | `GET /appointments` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Discounts](actions/list-discounts.md) | `GET /discounts` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Ratings](actions/list-ratings.md) | `GET /ratings/:accountNumber` | [docs](https://www.cituro.com/help/bewertungen-auf-webseite-einbinden) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
| [Search Customers](actions/search-customers.md) | `GET /customers` | [docs](https://www.cituro.com/help/developers-corner/schnittstellen) |
