# Tremendous: Native API Reference

A consolidated summary of Tremendous's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.tremendous.com/docs
- **API base URL:** `https://testflight.tremendous.com/api/v2`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://testflight.tremendous.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://testflight.tremendous.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `default team_management fraud_prevention`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://testflight.tremendous.com/oauth/token.

[Official authentication documentation](https://developers.tremendous.com/docs/oauth-20)

### API key

Uses a Tremendous API key as a bearer token for direct account access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.tremendous.com/docs/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://developers.tremendous.com/reference/create-campaign) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developers.tremendous.com/reference/create-order) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.tremendous.com/reference/create-webhook) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developers.tremendous.com/reference/delete-webhook) |
| [Retrieve Campaign](actions/get-campaign.md) | `GET /campaigns/:id` | [docs](https://developers.tremendous.com/reference/get-campaign) |
| [Retrieve Funding Source](actions/get-funding-source.md) | `GET /funding_sources/:id` | [docs](https://developers.tremendous.com/reference/get-funding-source) |
| [Retrieve Member](actions/get-member.md) | `GET /members/:id` | [docs](https://developers.tremendous.com/reference/get-member) |
| [Retrieve Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://developers.tremendous.com/reference/get-order) |
| [Retrieve Organization](actions/get-organization.md) | `GET /organizations/:id` | [docs](https://developers.tremendous.com/reference/get-organization) |
| [Retrieve Product](actions/get-product.md) | `GET /products/:id` | [docs](https://developers.tremendous.com/reference/get-product) |
| [Retrieve Reward](actions/get-reward.md) | `GET /rewards/:id` | [docs](https://developers.tremendous.com/reference/get-reward) |
| [Retrieve Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://developers.tremendous.com/reference/get-webhook) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.tremendous.com/reference/list-campaigns) |
| [List Funding Sources](actions/list-funding-sources.md) | `GET /funding_sources` | [docs](https://developers.tremendous.com/reference/list-funding-sources) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://developers.tremendous.com/reference/list-members) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.tremendous.com/reference/list-orders) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developers.tremendous.com/reference/list-organizations) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developers.tremendous.com/reference/list-products) |
| [List Rewards](actions/list-rewards.md) | `GET /rewards` | [docs](https://developers.tremendous.com/reference/list-rewards) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaigns/:id` | [docs](https://developers.tremendous.com/reference/update-campaign) |
