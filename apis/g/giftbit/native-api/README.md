# Giftbit: Native API Reference

A consolidated summary of Giftbit's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.giftbit.com/api-documentation
- **API base URL:** `https://api-testbed.giftbit.com/papi/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.giftbit.com/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Reward](actions/cancel-reward.md) | `DELETE /gifts/:uuid` | [docs](https://www.giftbit.com/api-documentation) |
| [Create Campaign Order](actions/create-campaign-order.md) | `POST /campaign` | [docs](https://www.giftbit.com/api-documentation) |
| [Create Direct Link Order](actions/create-direct-link-order.md) | `POST /direct_links` | [docs](https://www.giftbit.com/api-documentation) |
| [Create Embedded Reward](actions/create-embedded-reward.md) | `POST /embedded` | [docs](https://www.giftbit.com/api-documentation) |
| [Get Link URLs](actions/get-link-urls.md) | `GET /links/:id` | [docs](https://www.giftbit.com/api-documentation) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://www.giftbit.com/api-documentation) |
| [List Regions](actions/list-regions.md) | `GET /regions` | [docs](https://www.giftbit.com/api-documentation) |
| [List Rewards](actions/list-rewards.md) | `GET /gifts` | [docs](https://www.giftbit.com/api-documentation) |
| [Ping](actions/ping.md) | `GET /ping` | [docs](https://www.giftbit.com/api-documentation) |
| [Resend Reward](actions/resend-reward.md) | `PUT /gifts/:uuid` | [docs](https://www.giftbit.com/api-documentation) |
| [Retrieve Brand](actions/retrieve-brand.md) | `GET /brands/:brand_code` | [docs](https://www.giftbit.com/api-documentation) |
| [Retrieve Funding Information](actions/retrieve-funding-information.md) | `GET /funds` | [docs](https://www.giftbit.com/api-documentation) |
| [Retrieve Order by ID](actions/retrieve-order-by-id.md) | `GET /campaign/:id` | [docs](https://www.giftbit.com/api-documentation) |
| [Retrieve Reward](actions/retrieve-reward.md) | `GET /gifts/:uuid` | [docs](https://www.giftbit.com/api-documentation) |
