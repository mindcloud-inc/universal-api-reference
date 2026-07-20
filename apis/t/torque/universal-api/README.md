# <img src="https://images.mindcloud.co/apps/icons/torque-icon_1776367021740.png" alt="Torque logo" width="28" height="28"> Torque: Universal API

Torque provides crypto checkout, product checkout links, wallet analytics, routing, and business API tools for merchants and crypto applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/torque/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://torque.fi/
- **Vendor API docs:** https://docs.torque.fi/business/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Products](actions/get-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Aave Market

| Action | Method | Description |
| --- | --- | --- |
| [Get Aave Markets](actions/get-aave-markets.md) | GET |  |

### Approval Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Enso Approval Transaction](actions/get-enso-approval-transaction.md) | GET |  |

### Assistant Message

| Action | Method | Description |
| --- | --- | --- |
| [Chat With Assistant](actions/chat-with-assistant.md) | POST |  |

### Checkout Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Checkout Link](actions/generate-checkout-link.md) | POST |  |

### Checkout Session

| Action | Method | Description |
| --- | --- | --- |
| [Generate Checkout Session](actions/generate-checkout-session.md) | POST |  |

### Network

| Action | Method | Description |
| --- | --- | --- |
| [Get Enso Networks](actions/get-enso-networks.md) | GET |  |

### Non Tokenized Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Non Tokenized Positions](actions/get-non-tokenized-positions.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Status](actions/get-order-status.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [Get Products](actions/get-products.md) | GET |  |

### Subscription Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Products](actions/get-subscription-products.md) | GET |  |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Enso Tokens](actions/get-enso-tokens.md) | GET |  |

### Token Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Enso Balances](actions/get-enso-balances.md) | GET |  |

### Token Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Prices](actions/get-token-prices.md) | GET |  |

### Token Price History

| Action | Method | Description |
| --- | --- | --- |
| [Get Moralis Token Price History](actions/get-moralis-token-price-history.md) | GET |  |
| [Get Token Price History](actions/get-token-price-history.md) | GET |  |

### Tokenized Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Tokenized Positions](actions/get-tokenized-positions.md) | GET |  |

### Top Gaining Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Gaining Tokens](actions/get-top-gaining-tokens.md) | GET |  |

### Trade Route

| Action | Method | Description |
| --- | --- | --- |
| [Get Enso Routes](actions/get-enso-routes.md) | GET |  |

### Trending Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Trending Tokens](actions/get-trending-tokens.md) | GET |  |

### Wallet Pnl

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet PnL](actions/get-wallet-pnl.md) | GET |  |

### Wallet Token Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Moralis Balances](actions/get-moralis-balances.md) | GET |  |

### Wallet Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet History](actions/get-wallet-history.md) | GET |  |

