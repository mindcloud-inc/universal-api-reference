# Kiwify: Native API Reference

A consolidated summary of Kiwify's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.kiwify.com.br/api-reference/general
- **API base URL:** `https://public-api.kiwify.com`

## Authentication

### OAuth2 Client Credentials

Use your Kiwify client ID, client secret, and account ID. MindCloud exchanges the client credentials for an access token automatically.

### Credentials

- **Client ID:** `clientId` · required · Your Kiwify client_id used to request an access token.
- **Client Secret:** `clientSecret` · required · Your Kiwify client_secret used to request an access token.
- **Account ID:** `accountId` · required · Your Kiwify account_id, sent as the x-kiwify-account-id header on every request.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://public-api.kiwify.com/v1/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.kiwify.com.br/api-reference/auth/oauth)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Payout](actions/create-payout.md) | `POST /v1/payouts/` | [docs](https://docs.kiwify.com.br/api-reference/finance/payouts/create) |
| [Create Sale Refund](actions/create-sale-refund.md) | `POST /v1/sales/:id/refund` | [docs](https://docs.kiwify.com.br/api-reference/sales/refund) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://docs.kiwify.com.br/api-reference/webhooks/create) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:id` | [docs](https://docs.kiwify.com.br/api-reference/webhooks/delete) |
| [Get Account Details](actions/get-account-details.md) | `GET /v1/account-details` | [docs](https://docs.kiwify.com.br/api-reference/account/account-details) |
| [Get Affiliate](actions/get-affiliate.md) | `GET /v1/affiliates/:id` | [docs](https://docs.kiwify.com.br/api-reference/affiliates/single) |
| [Get Balance](actions/get-balance.md) | `GET /v1/balance/:legal_entity_id` | [docs](https://docs.kiwify.com.br/api-reference/finance/balance/single) |
| [Get Payout](actions/get-payout.md) | `GET /v1/payouts/:id` | [docs](https://docs.kiwify.com.br/api-reference/finance/payouts/single) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:id` | [docs](https://docs.kiwify.com.br/api-reference/products/single) |
| [Get Sale](actions/get-sale.md) | `GET /v1/sales/:id` | [docs](https://docs.kiwify.com.br/api-reference/sales/single) |
| [Get Sales Stats](actions/get-sales-stats.md) | `GET /v1/stats` | [docs](https://docs.kiwify.com.br/api-reference/sales/stats) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:id` | [docs](https://docs.kiwify.com.br/api-reference/webhooks/single) |
| [List Affiliates](actions/list-affiliates.md) | `GET /v1/affiliates` | [docs](https://docs.kiwify.com.br/api-reference/affiliates/list) |
| [List Balances](actions/list-balances.md) | `GET /v1/balance` | [docs](https://docs.kiwify.com.br/api-reference/finance/balance/list) |
| [List Event Participants](actions/list-event-participants.md) | `GET /v1/events/:product_id/participants` | [docs](https://docs.kiwify.com.br/api-reference/events/list) |
| [List Payouts](actions/list-payouts.md) | `GET /v1/payouts` | [docs](https://docs.kiwify.com.br/api-reference/finance/payouts/list) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://docs.kiwify.com.br/api-reference/products/list) |
| [List Sales](actions/list-sales.md) | `GET /v1/sales` | [docs](https://docs.kiwify.com.br/api-reference/sales/list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://docs.kiwify.com.br/api-reference/webhooks/list) |
| [Update Affiliate](actions/update-affiliate.md) | `PUT /v1/affiliates/:id` | [docs](https://docs.kiwify.com.br/api-reference/affiliates/edit) |
| [Update Webhook](actions/update-webhook.md) | `PUT /v1/webhooks/:id` | [docs](https://docs.kiwify.com.br/api-reference/webhooks/edit) |
