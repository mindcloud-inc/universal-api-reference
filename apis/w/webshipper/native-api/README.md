# Webshipper: Native API Reference

A consolidated summary of Webshipper's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://docs.webshipper.io/
- **OpenAPI specification:** https://docs.webshipper.io/?download_openapi=1
- **API base URL:** `https://{accountName}.api.webshipper.io/v2`

## Authentication

### Bearer Token

Use a Webshipper access token from Settings > Access and tokens.

### Credentials

- **API Key:** `apiKey` · required
- **Account Name:** `accountName` · required · Tenant account name used in the Webshipper subdomain and API base URL.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.webshipper.io/#2-authorisation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://docs.webshipper.io/#orders) |
| [Create Report](actions/create-report.md) | `POST /reports` | [docs](https://docs.webshipper.io/#reports) |
| [Create Return Cause](actions/create-return-cause.md) | `POST /return_causes` | [docs](https://docs.webshipper.io/#return_causes) |
| [Create Return Portal](actions/create-return-portal.md) | `POST /return_portals` | [docs](https://docs.webshipper.io/#return_portals) |
| [Create Return Shipping Method](actions/create-return-shipping-method.md) | `POST /return_shipping_methods` | [docs](https://docs.webshipper.io/#return_shipping_methods) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://docs.webshipper.io/#shipments) |
| [Create Shipping Rate](actions/create-shipping-rate.md) | `POST /shipping_rates` | [docs](https://docs.webshipper.io/#shipping_rates) |
| [Delete Shipping Rate](actions/delete-shipping-rate.md) | `DELETE /shipping_rates/:id` | [docs](https://docs.webshipper.io/#shipping_rates) |
| [Get Carrier](actions/get-carrier.md) | `GET /carriers/:id` | [docs](https://docs.webshipper.io/#carriers) |
| [Get Carrier Type](actions/get-carrier-type.md) | `GET /carrier_types/:id` | [docs](https://docs.webshipper.io/#carrier_types) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://docs.webshipper.io/#documents) |
| [Get Label](actions/get-label.md) | `GET /labels/:id` | [docs](https://docs.webshipper.io/#labels) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://docs.webshipper.io/#orders) |
| [Get Order Channel](actions/get-order-channel.md) | `GET /order_channels/:id` | [docs](https://docs.webshipper.io/#order_channels) |
| [Get Report](actions/get-report.md) | `GET /reports/:id` | [docs](https://docs.webshipper.io/#reports) |
| [Get Return Cause](actions/get-return-cause.md) | `GET /return_causes/:id` | [docs](https://docs.webshipper.io/#return_causes) |
| [Get Return Portal](actions/get-return-portal.md) | `GET /return_portals/:id` | [docs](https://docs.webshipper.io/#return_portals) |
| [Get Return Shipping Method](actions/get-return-shipping-method.md) | `GET /return_shipping_methods/:id` | [docs](https://docs.webshipper.io/#return_shipping_methods) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/:id` | [docs](https://docs.webshipper.io/#shipments) |
| [Get Shipping Rate](actions/get-shipping-rate.md) | `GET /shipping_rates/:id` | [docs](https://docs.webshipper.io/#shipping_rates) |
| [List Carrier Types](actions/list-carrier-types.md) | `GET /carrier_types` | [docs](https://docs.webshipper.io/#carrier_types) |
| [List Carriers](actions/list-carriers.md) | `GET /carriers` | [docs](https://docs.webshipper.io/#carriers) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.webshipper.io/#documents) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://docs.webshipper.io/#labels) |
| [List Order Channel Types](actions/list-order-channel-types.md) | `GET /order_channel_types` | [docs](https://docs.webshipper.io/#order_channel_types) |
| [List Order Channels](actions/list-order-channels.md) | `GET /order_channels` | [docs](https://docs.webshipper.io/#order_channels) |
| [List Order Documents](actions/list-order-documents.md) | `GET /orders/:id/documents` | [docs](https://docs.webshipper.io/#orders) |
| [List Order Print Jobs](actions/list-order-print-jobs.md) | `GET /orders/:id/print_jobs` | [docs](https://docs.webshipper.io/#orders) |
| [List Order Returns](actions/list-order-returns.md) | `GET /orders/:id/returns` | [docs](https://docs.webshipper.io/#orders) |
| [List Order Shipments](actions/list-order-shipments.md) | `GET /orders/:id/shipments` | [docs](https://docs.webshipper.io/#orders) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://docs.webshipper.io/#orders) |
| [List Printer Clients](actions/list-printer-clients.md) | `GET /printer_clients` | [docs](https://docs.webshipper.io/#printer_clients) |
| [List Printer Jobs](actions/list-printer-jobs.md) | `GET /printer_jobs` | [docs](https://docs.webshipper.io/#printer_jobs) |
| [List Reports](actions/list-reports.md) | `GET /reports` | [docs](https://docs.webshipper.io/#reports) |
| [List Return Causes](actions/list-return-causes.md) | `GET /return_causes` | [docs](https://docs.webshipper.io/#return_causes) |
| [List Return Portals](actions/list-return-portals.md) | `GET /return_portals` | [docs](https://docs.webshipper.io/#return_portals) |
| [List Return Shipments](actions/list-return-shipments.md) | `GET /shipments/:id/return_shipments` | [docs](https://docs.webshipper.io/#shipments) |
| [List Return Shipping Methods](actions/list-return-shipping-methods.md) | `GET /return_shipping_methods` | [docs](https://docs.webshipper.io/#return_shipping_methods) |
| [List Shipment Activities](actions/list-shipment-activities.md) | `GET /shipments/:id/activities` | [docs](https://docs.webshipper.io/#shipments) |
| [List Shipment Events](actions/list-shipment-events.md) | `GET /shipments/:id/events` | [docs](https://docs.webshipper.io/#shipments) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://docs.webshipper.io/#shipments) |
| [List Shipping Rates](actions/list-shipping-rates.md) | `GET /shipping_rates` | [docs](https://docs.webshipper.io/#shipping_rates) |
| [Quote Carrier Services](actions/quote-carrier-services.md) | `POST /service_quotes` | [docs](https://docs.webshipper.io/#service_quotes) |
| [Quote Order Channel Rates](actions/quote-order-channel-rates.md) | `POST /rate_quotes` | [docs](https://docs.webshipper.io/#rate_quotes) |
| [Update Order](actions/update-order.md) | `PATCH /orders/:id` | [docs](https://docs.webshipper.io/#orders) |
| [Update Return Cause](actions/update-return-cause.md) | `PATCH /return_causes/:id` | [docs](https://docs.webshipper.io/#return_causes) |
| [Update Return Portal](actions/update-return-portal.md) | `PATCH /return_portals/:id` | [docs](https://docs.webshipper.io/#return_portals) |
| [Update Return Shipping Method](actions/update-return-shipping-method.md) | `PATCH /return_shipping_methods/:id` | [docs](https://docs.webshipper.io/#return_shipping_methods) |
| [Update Shipment](actions/update-shipment.md) | `PATCH /shipments/:id` | [docs](https://docs.webshipper.io/#shipments) |
| [Update Shipping Rate](actions/update-shipping-rate.md) | `PATCH /shipping_rates/:id` | [docs](https://docs.webshipper.io/#shipping_rates) |
