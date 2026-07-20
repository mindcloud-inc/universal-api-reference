# Fintoc: Native API Reference

A consolidated summary of Fintoc's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.fintoc.com/reference
- **API base URL:** `https://api.fintoc.com`

## Authentication

### API Key

Use Fintoc Secret Key in Authorization header from backend requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.fintoc.com/docs/guides-api-keys)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Link Intent](actions/create-link-intent.md) | `POST /v1/link_intents` | [docs](https://docs.fintoc.com/reference/create-link-intent) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /v1/payment_links` | [docs](https://docs.fintoc.com/reference/create-payment-link) |
| [Create Transfer](actions/create-transfer.md) | `POST /v2/transfers` | [docs](https://docs.fintoc.com/reference/create-transfer-outbound) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /v1/webhook_endpoints` | [docs](https://docs.fintoc.com/reference/webhook-endpoints-create) |
| [Get Account](actions/get-account.md) | `GET /v2/accounts/:account_id` | [docs](https://docs.fintoc.com/reference/retrieve-account) |
| [Get Link](actions/get-link.md) | `GET /v1/links/:link_token` | [docs](https://docs.fintoc.com/reference/links-retrieve) |
| [Get Payment Intent](actions/get-payment-intent.md) | `GET /v1/payment_intents/:id` | [docs](https://docs.fintoc.com/reference/get-payment-intent) |
| [Get Transfer](actions/get-transfer.md) | `GET /v2/transfers/:transfer_id` | [docs](https://docs.fintoc.com/reference/retrieve-transfer) |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | `GET /v1/webhook_endpoints/:id` | [docs](https://docs.fintoc.com/reference/get-webhook-endpoints) |
| [List Accounts](actions/list-accounts.md) | `GET /v2/accounts` | [docs](https://docs.fintoc.com/reference/list-accounts) |
| [List Institutions](actions/list-institutions.md) | `GET /v1/institutions` | [docs](https://docs.fintoc.com/reference/list-institutions) |
| [List Links](actions/list-links.md) | `GET /v1/links` | [docs](https://docs.fintoc.com/reference/links-list) |
| [List Payment Intents](actions/list-payment-intents.md) | `GET /v1/payment_intents` | [docs](https://docs.fintoc.com/reference/list-payment-intents-copy) |
| [List Payment Links](actions/list-payment-links.md) | `GET /v1/payment_links` | [docs](https://docs.fintoc.com/reference/list-payment-links) |
| [List Transfers](actions/list-transfers.md) | `GET /v2/transfers` | [docs](https://docs.fintoc.com/reference/list-transfers) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /v1/webhook_endpoints` | [docs](https://docs.fintoc.com/reference/webhook-endpoints-list) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PATCH /v1/webhook_endpoints/:id` | [docs](https://docs.fintoc.com/reference/webhook-endpoints-update) |
