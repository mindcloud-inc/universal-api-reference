# Goldbelly: Native API Reference

A consolidated summary of Goldbelly's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing
- **API base URL:** `https://api.goldbelly.com/v1/`

## Authentication

### API Key

Authenticate requests with a Goldbelly 3PL API key using bearer authorization.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update Orders](actions/bulk-update-orders.md) | `POST orders/bulk_update` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#orders_bulk_update_post) |
| [Bulk Update Products](actions/bulk-update-products.md) | `POST products/bulk_update` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#products_bulk_update_post) |
| [Bulk Update Subproducts](actions/bulk-update-subproducts.md) | `POST subproducts/bulk_update` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#subproducts_bulk_update_post) |
| [Create Gift Card](actions/create-gift-card.md) | `POST gift_cards` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#gift_cards_post) |
| [Debit Gift Card](actions/debit-gift-card.md) | `POST gift_cards/:code/debits` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#gift_cards__code__debits_post) |
| [Get Gift Card](actions/get-gift-card.md) | `GET gift_cards/:code` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#gift_cards__code__get) |
| [Get Tracking](actions/get-tracking.md) | `GET tracking/:order_id` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#tracking__order_id__get) |
| [List Orders](actions/list-orders.md) | `GET orders` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#orders_get) |
| [List Products](actions/list-products.md) | `GET products` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#products_get) |
| [List Subproducts](actions/list-subproducts.md) | `GET subproducts` | [docs](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#subproducts_get) |
