# Gift Up: Native API Reference

A consolidated summary of Gift Up's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.giftup.com/api
- **API base URL:** `https://api.giftup.app`

## Authentication

### API Key

Authorize Gift Up requests with your Gift Up API key as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.giftup.com/api#authentication)

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://developer.giftup.com/api#create-a-new-item) |
| [Create Item Group](actions/create-item-group.md) | `POST /groups` | [docs](https://developer.giftup.com/api#create-an-item-group) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developer.giftup.com/api#create-an-order) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://developer.giftup.com/api#get-company) |
| [Get Gift Card by Code](actions/get-gift-card-by-code.md) | `GET /gift-cards/:code` | [docs](https://developer.giftup.com/api#get-a-gift-card-by-code) |
| [Get Item by ID](actions/get-item-by-id.md) | `GET /items/:id` | [docs](https://developer.giftup.com/api#get-an-item-by-id) |
| [Get Item Group by ID](actions/get-item-group-by-id.md) | `GET /groups/:id` | [docs](https://developer.giftup.com/api#get-an-item-group-by-id) |
| [Get Order by ID](actions/get-order-by-id.md) | `GET /orders/:id` | [docs](https://developer.giftup.com/api#get-an-order-by-id) |
| [Get Report Transaction](actions/get-report-transaction.md) | `GET /reports/transactions/:id` | [docs](https://developer.giftup.com/api#get-a-report-transaction) |
| [List Gift Cards](actions/list-gift-cards.md) | `GET /gift-cards` | [docs](https://developer.giftup.com/api#list-gift-cards) |
| [List Item Groups](actions/list-item-groups.md) | `GET /groups` | [docs](https://developer.giftup.com/api#list-all-item-groups) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://developer.giftup.com/api#list-all-items) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://developer.giftup.com/api#list-all-locations) |
| [List Report Transactions](actions/list-report-transactions.md) | `GET /reports/transactions` | [docs](https://developer.giftup.com/api#list-report-transactions) |
| [Reactivate Gift Card](actions/reactivate-gift-card.md) | `POST /gift-cards/:code/reactivate` | [docs](https://developer.giftup.com/api#reactivate-a-gift-card) |
| [Redeem Gift Card](actions/redeem-gift-card.md) | `POST /gift-cards/:code/redeem` | [docs](https://developer.giftup.com/api#redeem-a-gift-card) |
| [Redeem Gift Card in Full](actions/redeem-gift-card-in-full.md) | `POST /gift-cards/:code/redeem-in-full` | [docs](https://developer.giftup.com/api#redeem-a-gift-card-in-full) |
| [Top Up Gift Card](actions/top-up-gift-card.md) | `POST /gift-cards/:code/top-up` | [docs](https://developer.giftup.com/api#top-up-a-gift-card) |
| [Transfer Gift Card Balances](actions/transfer-gift-card-balances.md) | `POST /gift-cards/transfer-balances` | [docs](https://developer.giftup.com/api#transfer-balances-between-gift-cards) |
| [Undo Gift Card Redemption](actions/undo-gift-card-redemption.md) | `POST /gift-cards/:code/undo-redemption` | [docs](https://developer.giftup.com/api#undo-a-redemption) |
| [Update Gift Card](actions/update-gift-card.md) | `PATCH /gift-cards/:code` | [docs](https://developer.giftup.com/api#update-a-gift-card) |
| [Update Item](actions/update-item.md) | `PATCH /items/:id` | [docs](https://developer.giftup.com/api#update-an-item) |
| [Update Item Group](actions/update-item-group.md) | `PATCH /groups/:id` | [docs](https://developer.giftup.com/api#update-an-item-group) |
| [Void Gift Card](actions/void-gift-card.md) | `POST /gift-cards/:code/void` | [docs](https://developer.giftup.com/api#void-a-gift-card) |
