# Referral Factory: Native API Reference

A consolidated summary of Referral Factory's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developers.referral-factory.com/reference
- **API base URL:** `https://referral-factory.com/api/v2`

## Authentication

### API Access Token

Connect Referral Factory with your API access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.referral-factory.com/reference/obtain-api-keys)

## API conventions

Response data is read from `data`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; maximum 250). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.referral-factory.com/reference/list-all-campaigns) |
| [List Due Rewards](actions/list-due-rewards.md) | `GET /rewards/due/:metric` | [docs](https://developers.referral-factory.com/reference/list-all-due-rewards) |
| [List Issued Rewards](actions/list-issued-rewards.md) | `GET /rewards/issued/:metric` | [docs](https://developers.referral-factory.com/reference/list-all-issued-rewards) |
| [List Rewards](actions/list-rewards.md) | `GET /rewards/dashboard/:metric` | [docs](https://developers.referral-factory.com/reference/list-all-rewards) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.referral-factory.com/reference/list-all-users) |
| [Retrieve Campaign](actions/retrieve-campaign.md) | `GET /campaigns/:identifier` | [docs](https://developers.referral-factory.com/reference/retrieve-a-campaign) |
| [Search Campaigns](actions/search-campaigns.md) | `POST /campaigns/search` | [docs](https://developers.referral-factory.com/reference/search-campaigns) |
| [Search Due Rewards](actions/search-due-rewards.md) | `POST /rewards/due/:metric/search` | [docs](https://developers.referral-factory.com/reference/search-rewards-due) |
| [Search Issued Rewards](actions/search-issued-rewards.md) | `POST /rewards/issued/:metric/search` | [docs](https://developers.referral-factory.com/reference/search-rewards-issued) |
| [Search Rewards](actions/search-rewards.md) | `POST /rewards/dashboard/:metric/search` | [docs](https://developers.referral-factory.com/reference/search-rewards) |
| [Search Users](actions/search-users.md) | `POST /users/search` | [docs](https://developers.referral-factory.com/reference/search-users) |
