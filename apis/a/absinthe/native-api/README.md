# Absinthe: Native API Reference

A consolidated summary of Absinthe's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.absinthe.network/doc
- **OpenAPI specification:** https://api.absinthe.network/doc
- **API base URL:** `https://api.absinthe.network`

## Authentication

### API Key

Authenticate with an Absinthe workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://guides.absinthe.network/integrations/api/points_api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Inventory Item](actions/archive-inventory-item.md) | `DELETE /inventory/{inventory_id}` | [docs](https://api.absinthe.network/doc) |
| [Claim Badge](actions/claim-badge.md) | `POST /badges/{badge_id}/claim` | [docs](https://api.absinthe.network/doc) |
| [Create Badge](actions/create-badge.md) | `POST /badges` | [docs](https://api.absinthe.network/doc) |
| [Create Inventory Item](actions/create-inventory-item.md) | `POST /inventory` | [docs](https://api.absinthe.network/doc) |
| [Create Registered Event](actions/create-registered-event.md) | `POST /events` | [docs](https://api.absinthe.network/doc) |
| [Delete Badge](actions/delete-badge.md) | `DELETE /badges/{badge_id}` | [docs](https://api.absinthe.network/doc) |
| [Get Badge](actions/get-badge.md) | `GET /badges/{badge_id}` | [docs](https://api.absinthe.network/doc) |
| [Get Badge Status](actions/get-badge-status.md) | `GET /badges/{badge_id}/status` | [docs](https://api.absinthe.network/doc) |
| [Get Campaign Redemptions](actions/get-campaign-redemptions.md) | `GET /redemptions/campaign` | [docs](https://api.absinthe.network/doc) |
| [Get Leaderboard](actions/get-leaderboard.md) | `GET /leaderboard` | [docs](https://api.absinthe.network/doc) |
| [Get Leaderboard Stats](actions/get-leaderboard-stats.md) | `GET /leaderboard/stats` | [docs](https://api.absinthe.network/doc) |
| [Get User Identities](actions/get-user-identities.md) | `GET /users/{user_id}` | [docs](https://api.absinthe.network/doc) |
| [Get User Point Sources](actions/get-user-point-sources.md) | `GET /users/{user_id}/point-sources` | [docs](https://api.absinthe.network/doc) |
| [Get User Redemptions](actions/get-user-redemptions.md) | `GET /redemptions/users/{user_id}/redemptions` | [docs](https://api.absinthe.network/doc) |
| [Get User Scores](actions/get-user-scores.md) | `GET /users/{user_id}/scores` | [docs](https://api.absinthe.network/doc) |
| [Get User XP Balance](actions/get-user-xp-balance.md) | `GET /redemptions/users/{user_id}/balance` | [docs](https://api.absinthe.network/doc) |
| [List Active Inventory Items](actions/list-active-inventory-items.md) | `GET /inventory/public` | [docs](https://api.absinthe.network/doc) |
| [List Badges](actions/list-badges.md) | `GET /badges` | [docs](https://api.absinthe.network/doc) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://api.absinthe.network/doc) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /inventory` | [docs](https://api.absinthe.network/doc) |
| [List Point Sources](actions/list-point-sources.md) | `GET /point-sources` | [docs](https://api.absinthe.network/doc) |
| [List Registered Events](actions/list-registered-events.md) | `GET /events` | [docs](https://api.absinthe.network/doc) |
| [Redeem an Item](actions/redeem-an-item.md) | `POST /redemptions/users/{user_id}/redeem` | [docs](https://api.absinthe.network/doc) |
| [Refund a Redemption](actions/refund-a-redemption.md) | `POST /redemptions/{redemption_id}/refund` | [docs](https://api.absinthe.network/doc) |
| [Resolve Identity to User ID](actions/resolve-identity-to-user-id.md) | `GET /users/resolve` | [docs](https://api.absinthe.network/doc) |
| [Submit Event Data](actions/submit-event-data.md) | `POST /events/{event_id}/data` | [docs](https://api.absinthe.network/doc) |
| [Update Badge](actions/update-badge.md) | `PUT /badges/{badge_id}` | [docs](https://api.absinthe.network/doc) |
| [Update Inventory Item](actions/update-inventory-item.md) | `PATCH /inventory/{inventory_id}` | [docs](https://api.absinthe.network/doc) |
| [Update Redemption Status](actions/update-redemption-status.md) | `PATCH /redemptions/{redemption_id}` | [docs](https://api.absinthe.network/doc) |
| [Upload Badge Image](actions/upload-badge-image.md) | `POST /badges/upload-image` | [docs](https://api.absinthe.network/doc) |
