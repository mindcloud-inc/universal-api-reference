# Facebook: Native API Reference

A consolidated summary of Facebook's API configuration and 3 documented operations.

- **API base URL:** `https://graph.facebook.com/v23.0/`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.facebook.com/v24.0/dialog/oauth to approve access.
2. Exchange the returned authorization code with a GET request to https://graph.facebook.com/v24.0/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `pages_read_user_content read_insights pages_read_engagement ads_read pages_show_list business_management`.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (3 documented)

| Operation | Method & path |
| --- | --- |
| [Ad Campaign Query](actions/ad-campaign-query.md) | `GET :accountID/?fields=id,account_id,name,account_status,business,balance,amount_spent` |
| [Get Owned Pages](actions/get-owned-pages.md) | `GET :businessId/owned_pages?fields=id,name,access_token` |
| [Get Page Ratings](actions/get-page-ratings.md) | `GET :pageId/ratings` |
