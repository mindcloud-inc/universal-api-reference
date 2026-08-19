# Facebook: Native API Reference

A consolidated summary of Facebook's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developers.facebook.com/docs/
- **API base URL:** `https://graph.facebook.com/v25.0`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.facebook.com/v24.0/dialog/oauth to approve access.
2. Exchange the returned authorization code with a GET request to https://graph.facebook.com/v24.0/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `pages_read_user_content read_insights pages_read_engagement ads_read pages_show_list business_management`.

[Official authentication documentation](https://developers.facebook.com/documentation/facebook-login/guides/access-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size. Use `after` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ad Account Ads Query](actions/ad-account-ads-query.md) | `GET https://graph.facebook.com/v23.0/:adAccountID/ads` |  |
| [Ad Campaign Query](actions/ad-campaign-query.md) | `GET /:accountID` |  |
| [Get Owned Pages](actions/get-owned-pages.md) | `GET :businessId/owned_pages?fields=id,name,access_token` |  |
| [Get Page](actions/get-page.md) | `GET :pageId` | [docs](https://developers.facebook.com/docs/graph-api/reference/page/) |
| [Get Page Insights](actions/get-page-insights.md) | `GET /:pageId/insights` | [docs](https://developers.facebook.com/docs/graph-api/reference/v25.0/insights) |
| [List Ad Accounts](actions/list-ad-accounts.md) | `GET me/adaccounts` | [docs](https://developers.facebook.com/docs/graph-api/reference/user/adaccounts/) |
| [List Businesses](actions/list-businesses.md) | `GET /me/businesses` | [docs](https://developers.facebook.com/docs/graph-api/reference/user/businesses/) |
| [List Pages](actions/list-pages.md) | `GET me/accounts` | [docs](https://developers.facebook.com/docs/graph-api/reference/user/accounts/) |
