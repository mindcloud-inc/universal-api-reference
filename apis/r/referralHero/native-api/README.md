# ReferralHero: Native API Reference

A consolidated summary of ReferralHero's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://support.referralhero.com/integrate/rest-api
- **API base URL:** `https://app.referralhero.com/api/v2`

## Authentication

### API Token

Connect ReferralHero with an API token from Account > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.referralhero.com/integrate/rest-api/endpoints-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.pagination.totalPages`. The current page number is read from `data.pagination.currentPage`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | `POST /lists/:uuid/subscribers` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-coupons) |
| [Create Coupon Group](actions/create-coupon-group.md) | `POST /lists/:uuid/coupon_groups` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#create-coupon-group) |
| [Create Coupons](actions/create-coupons.md) | `POST /lists/:uuid/coupons` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#create-coupons) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#create-a-new-list) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /lists/:uuid/subscribers/:subscriber_id` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-subscriber-by-mwr) |
| [Get List Leaderboard](actions/get-list-leaderboard.md) | `GET /lists/:uuid/leaderboard` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#get-list-leaderboard) |
| [List All Level 2 Referrals](actions/list-all-level2-referrals.md) | `GET /lists/:uuid/subscribers/:subscriber_id/level_2_all_referrals` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-referrals-pending-unconfirmed-confirmed-of-a-subscriber) |
| [List Coupon Groups](actions/list-coupon-groups.md) | `GET /lists/:uuid/coupon_groups` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-coupon-groups) |
| [List Coupons](actions/list-coupons.md) | `GET /lists/:uuid/coupon_groups/:id` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-coupon-groups) |
| [List Level 1 Referrals](actions/list-level1-referrals.md) | `GET /lists/:uuid/subscribers/:subscriber_id/level_1_referrals` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-level-2-referrals-pending-unconfirmed-confirmed-of-a-subscriber) |
| [List Level 2 Referrals](actions/list-level2-referrals.md) | `GET /lists/:uuid/subscribers/:subscriber_id/level_2_referrals` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-level-1-confirmed-referrals-of-a-subscriber) |
| [List Level 3 Referrals](actions/list-level3-referrals.md) | `GET /lists/:uuid/subscribers/:subscriber_id/level_3_referrals` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-level-2-confirmed-referrals-of-a-subscriber) |
| [List List Rewards](actions/list-list-rewards.md) | `GET /lists/:uuid/bonuses` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#get-list-rewards) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-lists) |
| [List Referred Subscribers](actions/list-referred-subscribers.md) | `GET /lists/:uuid/subscribers/:subscriber_id/referred` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#track-bulk-transactions) |
| [List Rewards for All Subscribers](actions/list-rewards-for-all-subscribers.md) | `GET /lists/:uuid/rewards` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-rewards-for-all-subscribers) |
| [List Subscriber Rewards](actions/list-subscriber-rewards.md) | `GET /lists/:uuid/subscribers/:subscriber_id/rewards` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#delete-a-subscriber) |
| [List Subscribers](actions/list-subscribers.md) | `GET /lists/:uuid/subscribers` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-coupon-groups) |
| [Retrieve Subscriber by Email](actions/retrieve-subscriber-by-email.md) | `GET /lists/:uuid/subscribers/retrieve_by_email` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-subscriber-by-id) |
| [Retrieve Subscriber by ID](actions/retrieve-subscriber-by-id.md) | `GET /lists/:uuid/subscribers/:subscriber_id` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-subscribers-from-a-list) |
| [Retrieve Subscriber by MWR](actions/retrieve-subscriber-by-mwr.md) | `GET /lists/:uuid/subscribers/retrieve_by_mwr` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-subscriber-by-email) |
| [Track Bulk Transactions](actions/track-bulk-transactions.md) | `POST /lists/:uuid/subscribers/add_bulk_transactions` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#track-transactions-single-transaction) |
| [Track Single Transaction](actions/track-single-transaction.md) | `POST /lists/:uuid/subscribers/add_transactions` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-rewards-unlocked-by-a-subscriber) |
| [Update Subscriber](actions/update-subscriber.md) | `POST /lists/:uuid/subscribers/:subscriber_id` | [docs](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#add-a-subscriber) |
