# Torque: Native API Reference

A consolidated summary of Torque's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.torque.fi/business/api-reference
- **API base URL:** `https://app.torque.fi/api`

## Authentication

### API Key

Use a Torque Business API key. Torque expects requests to include Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required
- **Business ID:** `businessId` · required · Torque Business ID used by product and checkout endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.torque.fi/business/api-reference)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chat With Assistant](actions/chat-with-assistant.md) | `POST /assistant/chat` | [docs](https://docs.torque.fi/business/api-reference) |
| [Generate Checkout Link](actions/generate-checkout-link.md) | `POST /checkout/generate-link` | [docs](https://docs.torque.fi/business/api-reference) |
| [Generate Checkout Session](actions/generate-checkout-session.md) | `POST /torque-checkout` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Aave Markets](actions/get-aave-markets.md) | `GET /enso/aave-markets` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Enso Approval Transaction](actions/get-enso-approval-transaction.md) | `POST /enso/approval` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Enso Balances](actions/get-enso-balances.md) | `GET /enso/balances` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Enso Networks](actions/get-enso-networks.md) | `GET /enso/networks` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Enso Routes](actions/get-enso-routes.md) | `POST /enso/routes` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Enso Tokens](actions/get-enso-tokens.md) | `GET /enso/tokens` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Moralis Balances](actions/get-moralis-balances.md) | `GET /moralis/balances` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Moralis Token Price History](actions/get-moralis-token-price-history.md) | `GET /moralis/token-price-history` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Non Tokenized Positions](actions/get-non-tokenized-positions.md) | `GET /enso/positions/nontokenized` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Order Status](actions/get-order-status.md) | `GET /checkout/order-status/:orderId` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Product](actions/get-product.md) | `GET /products/:productId` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Products](actions/get-products.md) | `GET /products` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Subscription Products](actions/get-subscription-products.md) | `GET /products/subscriptions` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Token Price History](actions/get-token-price-history.md) | `GET /token-price-history` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Token Prices](actions/get-token-prices.md) | `GET /token-prices` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Tokenized Positions](actions/get-tokenized-positions.md) | `GET /enso/positions/tokenized` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Top Gaining Tokens](actions/get-top-gaining-tokens.md) | `GET /moralis/token-top-gainers` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Trending Tokens](actions/get-trending-tokens.md) | `GET /moralis/trending-tokens` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Wallet History](actions/get-wallet-history.md) | `GET /moralis/wallet-history` | [docs](https://docs.torque.fi/business/api-reference) |
| [Get Wallet PnL](actions/get-wallet-pnl.md) | `GET /moralis/wallet-pnl` | [docs](https://docs.torque.fi/business/api-reference) |
