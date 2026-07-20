# Reward Sciences: Native API Reference

A consolidated summary of Reward Sciences's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://developers.rewardsciences.com/api/docs
- **API base URL:** `https://api.rewardsciences.com`

## Authentication

### API Token

Reward Sciences API token from Developer Settings > API Tokens.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.rewardsciences.com/api/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.rewardsciences.v2+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign External Identity To User](actions/assign-external-identity-to-user.md) | `POST /users/:userId/identities` | [docs](https://developers.rewardsciences.com/api/docs#assigning-external-identities-to-a-user-assign-a-new-external-identity-to-a-user) |
| [Bid On Reward](actions/bid-on-reward.md) | `POST /rewards/:rewardId/bids` |  |
| [Create User By External Identity](actions/create-user-by-external-identity.md) | `POST /idps/:idp/:identity/user` | [docs](https://developers.rewardsciences.com/api/docs#managing-users-using-external-identities-create-a-user-using-an-external-identity) |
| [Get Reward](actions/get-reward.md) | `GET /rewards/:rewardId` |  |
| [Get User](actions/get-user.md) | `GET /users/:userId` |  |
| [Get User By External Identity](actions/get-user-by-external-identity.md) | `GET /idps/:idp/:identity/user` | [docs](https://developers.rewardsciences.com/api/docs#managing-users-using-external-identities-fetch-user-info-using-external-identity) |
| [List Reward Categories](actions/list-reward-categories.md) | `GET /reward_categories` |  |
| [List Rewards](actions/list-rewards.md) | `GET /rewards` |  |
| [Redeem Reward](actions/redeem-reward.md) | `POST /rewards/:rewardId/redemptions` |  |
| [Track Activity](actions/track-activity.md) | `POST /activities` | [docs](https://developers.rewardsciences.com/api/docs#tracking-user-activities) |
