# Ship&Co: Native API Reference

A consolidated summary of Ship&Co's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developer.shipandco.com/en/
- **API base URL:** `https://api.shipandco.com/v1`

## Authentication

### API Token

Authenticate Ship&Co requests with the API token generated from the Ship&Co dashboard. Requests send the token in the x-access-token header.

### Credentials

- **API Key:** `apiKey` · required · Ship&Co API token copied from the dashboard API page. Sent as the x-access-token request header.

Send these headers with each API request:

```http
x-access-token: <apiKey>
```

[Official authentication documentation](https://developer.shipandco.com/en/#authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developer.shipandco.com/en/#order) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://developer.shipandco.com/en/#shipment) |
| [Delete Carrier](actions/delete-carrier.md) | `DELETE /carriers/:id` | [docs](https://developer.shipandco.com/en/#carrier) |
| [Delete Negotiated Rates](actions/delete-negotiated-rates.md) | `DELETE /carriers/:id/rates` | [docs](https://developer.shipandco.com/en/#negotiated-rates) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/:id` | [docs](https://developer.shipandco.com/en/#order) |
| [Delete Shipment](actions/delete-shipment.md) | `DELETE /shipments/:id` | [docs](https://developer.shipandco.com/en/#shipment) |
| [Delete Sub User](actions/delete-sub-user.md) | `DELETE /sub-users/:id` | [docs](https://developer.shipandco.com/en/#sub-user) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/:id` | [docs](https://developer.shipandco.com/en/#shipment) |
| [Get Sub User](actions/get-sub-user.md) | `GET /sub-users/:id` | [docs](https://developer.shipandco.com/en/#sub-user) |
| [Get Tracking](actions/get-tracking.md) | `GET /tracking/:carrier/:trackingNumber` | [docs](https://developer.shipandco.com/en/#tracking) |
| [List Carriers](actions/list-carriers.md) | `GET /carriers` | [docs](https://developer.shipandco.com/en/#carrier) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://developer.shipandco.com/en/#files) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developer.shipandco.com/en/#order) |
| [List Rates](actions/list-rates.md) | `POST /rates` | [docs](https://developer.shipandco.com/en/#rates) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://developer.shipandco.com/en/#shipment) |
| [List Shipping Addresses](actions/list-shipping-addresses.md) | `GET /addresses` | [docs](https://developer.shipandco.com/en/#shipping-address) |
| [List Sub Users](actions/list-sub-users.md) | `GET /sub-users` | [docs](https://developer.shipandco.com/en/#sub-user) |
| [List Warehouses](actions/list-warehouses.md) | `GET /warehouses` | [docs](https://developer.shipandco.com/en/#warehouse) |
| [Regenerate Sub User API Token](actions/regenerate-sub-user-api-token.md) | `POST /sub-users/:id` | [docs](https://developer.shipandco.com/en/#sub-user) |
| [Register Carrier](actions/register-carrier.md) | `POST /carriers` | [docs](https://developer.shipandco.com/en/#carrier) |
| [Register Shipping Address](actions/register-shipping-address.md) | `POST /addresses` | [docs](https://developer.shipandco.com/en/#shipping-address) |
| [Register Sub User](actions/register-sub-user.md) | `POST /sub-users` | [docs](https://developer.shipandco.com/en/#sub-user) |
| [Register Warehouse](actions/register-warehouse.md) | `POST /warehouses` | [docs](https://developer.shipandco.com/en/#warehouse) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://developer.shipandco.com/en/#files) |
| [Upload Negotiated Rates](actions/upload-negotiated-rates.md) | `POST /carriers/:id/rates` | [docs](https://developer.shipandco.com/en/#negotiated-rates) |
