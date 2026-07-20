# GoAffPro: Native API Reference

A consolidated summary of GoAffPro's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.goaffpro.com/docs/admin/
- **API base URL:** `https://api.goaffpro.com/v1`

## Authentication

### Access Token

Connect with a GoAffPro store access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-goaffpro-access-token: <apiKey>
```

[Official authentication documentation](https://api.goaffpro.com/docs/admin/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–250). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort_column` in the query string. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Affiliate](actions/create-affiliate.md) | `POST /admin/affiliates` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Create Order](actions/create-order.md) | `POST /admin/orders` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Create Payment Request](actions/create-payment-request.md) | `POST /admin/payments/requests` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Give Reward](actions/give-reward.md) | `POST /admin/rewards` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Affiliate Coupons](actions/list-affiliate-coupons.md) | `GET /admin/affiliates/:id/coupons` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Affiliate Customer Connections](actions/list-affiliate-customer-connections.md) | `GET /admin/connections` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Affiliate Referral Codes](actions/list-affiliate-referral-codes.md) | `GET /admin/affiliates/:id/referral_codes` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Affiliates](actions/list-affiliates.md) | `GET /admin/affiliates` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Coupon Codes](actions/list-coupon-codes.md) | `GET /admin/coupons` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Groups](actions/list-groups.md) | `GET /admin/groups` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Orders](actions/list-orders.md) | `GET /admin/orders` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Payment Requests](actions/list-payment-requests.md) | `GET /admin/payments/requests` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Payments](actions/list-payments.md) | `GET /admin/payments` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Pending Payouts](actions/list-pending-payouts.md) | `GET /admin/payments/pending` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Rewards](actions/list-rewards.md) | `GET /admin/rewards` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Traffic](actions/list-traffic.md) | `GET /admin/traffic` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Transactions](actions/list-transactions.md) | `GET /admin/transactions` | [docs](https://api.goaffpro.com/docs/admin/) |
| [List Unpaid Transactions](actions/list-unpaid-transactions.md) | `GET /admin/payments/transactions/unpaid` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Recalculate Order Commission](actions/recalculate-order-commission.md) | `POST /admin/orders/recalculate/:id` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Replace Affiliate Referral Codes](actions/replace-affiliate-referral-codes.md) | `PUT /admin/affiliates/:id/referral_codes` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Search Affiliates](actions/search-affiliates.md) | `GET /admin/affiliates/search` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Update Affiliate](actions/update-affiliate.md) | `PATCH /admin/affiliates/:id` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Update Order](actions/update-order.md) | `PATCH /admin/orders/:id` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Update Payment Request](actions/update-payment-request.md) | `PATCH /admin/payments/requests/:id` | [docs](https://api.goaffpro.com/docs/admin/) |
| [Update Reward](actions/update-reward.md) | `PATCH /admin/rewards/:id` | [docs](https://api.goaffpro.com/docs/admin/) |
