# SendBox: Native API Reference

A consolidated summary of SendBox's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.sendbox.co/
- **API base URL:** `https://live.sendbox.co`

## Authentication

### Access Token

Use the permanent Sendbox access token. Sendbox requires the raw token in the Authorization header, without a Bearer prefix.

### Credentials

- **Access Token:** `accessToken` · required · Permanent Sendbox access token used as the raw Authorization header value for every request.

Send these headers with each API request:

```http
Authorization: <accessToken>
```

[Official authentication documentation](https://docs.sendbox.co/authentication/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Landed Cost](actions/calculate-landed-cost.md) | `POST /shipping/landed_cost_estimate` | [docs](https://docs.sendbox.co/shipping/calculate-landed-cost) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipping/shipments` | [docs](https://docs.sendbox.co/shipping/create-new-shipment) |
| [Get Payment Profile](actions/get-payment-profile.md) | `GET /payments/profile` | [docs](https://docs.sendbox.co/payment/payment-profile) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipping/shipments/:id` | [docs](https://docs.sendbox.co/shipping/get-shipment) |
| [List Saved Addresses](actions/list-saved-addresses.md) | `GET /auth/addresses` | [docs](https://docs.sendbox.co/shipping/saved-addresses) |
| [List Shipments](actions/list-shipments.md) | `GET /shipping/shipments` | [docs](https://docs.sendbox.co/shipping/get-shipments) |
| [List Virtual Accounts](actions/list-virtual-accounts.md) | `GET /payments/virtual_accounts` | [docs](https://docs.sendbox.co/payment/virtual-account) |
| [Request Shipping Quotes](actions/request-shipping-quotes.md) | `POST /shipping/shipment_delivery_quote` | [docs](https://docs.sendbox.co/shipping/request-shipping-quotes) |
| [Track Shipment](actions/track-shipment.md) | `POST /shipping/tracking` | [docs](https://docs.sendbox.co/shipping/track-shipment) |
