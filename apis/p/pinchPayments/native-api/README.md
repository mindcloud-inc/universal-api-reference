# Pinch Payments: Native API Reference

A consolidated summary of Pinch Payments's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.getpinch.com.au/reference
- **API base URL:** `https://api.getpinch.com.au/live`

## Authentication

### OAuth2 Client Credentials

Use a Pinch Merchant ID or Application ID with the matching secret to mint bearer tokens for the Pinch API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.getpinch.com.au/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.getpinch.com.au/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `api1`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.getpinch.com.au/docs/application-authentication)

## API conventions

The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create or Update Payer](actions/create-or-update-payer.md) | `POST /payers` | [docs](https://docs.getpinch.com.au/reference/save-payer) |
| [Create or Update Payment](actions/create-or-update-payment.md) | `POST /payments` | [docs](https://docs.getpinch.com.au/reference/save-payment) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /payment-links` | [docs](https://docs.getpinch.com.au/reference/create-payment-link) |
| [Create Payment Source](actions/create-payment-source.md) | `POST /payers/[:id]/sources` | [docs](https://docs.getpinch.com.au/reference/create-payment-source) |
| [Create Realtime Payment](actions/create-realtime-payment.md) | `POST /payments/realtime` | [docs](https://docs.getpinch.com.au/reference/realtime-payment) |
| [Create Refund](actions/create-refund.md) | `POST /refunds` | [docs](https://docs.getpinch.com.au/reference/create-a-refund) |
| [Delete Payer](actions/delete-payer.md) | `DELETE /payers/[:id]` | [docs](https://docs.getpinch.com.au/reference/delete-payer) |
| [Delete Payment](actions/delete-payment.md) | `DELETE /payments/[:id]` | [docs](https://docs.getpinch.com.au/reference/delete-payment) |
| [Delete Payment Link](actions/delete-payment-link.md) | `DELETE /payment-links/[:id]` | [docs](https://docs.getpinch.com.au/reference/delete-payment-link) |
| [Delete Payment Source](actions/delete-payment-source.md) | `DELETE /payers/[:id]/sources/[:sourceId]` | [docs](https://docs.getpinch.com.au/reference/delete-payment-source) |
| [Get Event](actions/get-event.md) | `GET /events/[:id]` | [docs](https://docs.getpinch.com.au/reference/get-event) |
| [Get Merchant](actions/get-merchant.md) | `GET /merchants` | [docs](https://docs.getpinch.com.au/reference/list-merchants) |
| [Get Payer](actions/get-payer.md) | `GET /payers/[:id]` | [docs](https://docs.getpinch.com.au/reference/get-payer) |
| [Get Payment](actions/get-payment.md) | `GET /payments/[:id]` | [docs](https://docs.getpinch.com.au/reference/get-payment) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /payment-links/[:id]` | [docs](https://docs.getpinch.com.au/reference/get-payment-link) |
| [Get Refund](actions/get-refund.md) | `GET /refund/[:id]` | [docs](https://docs.getpinch.com.au/reference/get-refund) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.getpinch.com.au/reference/list-all-events) |
| [List Payers](actions/list-payers.md) | `GET /payers` | [docs](https://docs.getpinch.com.au/reference/list-payers) |
| [List Payment Links](actions/list-payment-links.md) | `GET /payment-links` | [docs](https://docs.getpinch.com.au/reference/get-payment-links) |
| [List Payment Links for Payer](actions/list-payment-links-for-payer.md) | `GET /payment-links/payer/[:payerId]` | [docs](https://docs.getpinch.com.au/reference/get-payment-links-by-payer) |
| [List Payments for Payer](actions/list-payments-for-payer.md) | `GET /payments/payer/[:id]` | [docs](https://docs.getpinch.com.au/reference/list-payments-for-payer) |
| [List Processed Payments](actions/list-processed-payments.md) | `GET /payments/processed` | [docs](https://docs.getpinch.com.au/reference/list-processed-payments) |
| [List Refunds](actions/list-refunds.md) | `GET /refunds` | [docs](https://docs.getpinch.com.au/reference/list-refunds) |
| [List Scheduled Payments](actions/list-scheduled-payments.md) | `GET /payments/scheduled` | [docs](https://docs.getpinch.com.au/reference/list-scheduled-payments) |
