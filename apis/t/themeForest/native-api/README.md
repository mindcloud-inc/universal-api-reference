# Themeforest: Native API Reference

A consolidated summary of Themeforest's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://build.envato.com/api/
- **OpenAPI specification:** https://api.envato.com/api-docs
- **API base URL:** `https://api.envato.com`

## Authentication

### Envato OAuth2

Connect with an Envato account to access ThemeForest and Envato Market data.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.envato.com/authorization to approve access.
2. Exchange the returned authorization code with a POST request to https://api.envato.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `default user:username user:email user:account user:financial purchase:download purchase:list purchase:history sale:history sale:verify user:collections user:statement`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.envato.com/token.

[Official authentication documentation](https://build.envato.com/api/#oauth)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Similar Items](actions/find-similar-items.md) | `GET /v1/discovery/search/search/more_like_this` | [docs](https://build.envato.com/api/#search_getSearchMoreLikeThis) |
| [Get Account](actions/get-account.md) | `GET /v1/market/private/user/account.json` | [docs](https://build.envato.com/api/#market_getUserAccount) |
| [Get Account Email](actions/get-account-email.md) | `GET /v1/market/private/user/email.json` | [docs](https://build.envato.com/api/#market_getUserEmail) |
| [Get Account Username](actions/get-account-username.md) | `GET /v1/market/private/user/username.json` | [docs](https://build.envato.com/api/#market_getUserUsername) |
| [Get Catalog Collection](actions/get-catalog-collection.md) | `GET /v3/market/catalog/collection` | [docs](https://build.envato.com/api/#market_0_getCatalogCollection) |
| [Get Catalog Item](actions/get-catalog-item.md) | `GET /v3/market/catalog/item` | [docs](https://build.envato.com/api/#market_0_getCatalogItem) |
| [Get Catalog Item Version](actions/get-catalog-item-version.md) | `GET /v3/market/catalog/item-version` | [docs](https://build.envato.com/api/#market_0_getCatalogItemVersion) |
| [Get Item Prices](actions/get-item-prices.md) | `GET /v1/market/item-prices::item_id.json` | [docs](https://build.envato.com/api/#market_getItemPrices) |
| [Get New Files From User](actions/get-new-files-from-user.md) | `GET /v1/market/new-files-from-user::username,:site.json` | [docs](https://build.envato.com/api/#market_getNewFilesFromUser) |
| [Get ThemeForest Categories](actions/get-themeforest-categories.md) | `GET /v1/market/categories::site.json` | [docs](https://build.envato.com/api/#market_getCategories) |
| [Get ThemeForest Featured Items](actions/get-themeforest-featured-items.md) | `GET /v1/market/features::site.json` | [docs](https://build.envato.com/api/#market_getFeatures) |
| [Get ThemeForest File Counts](actions/get-themeforest-file-counts.md) | `GET /v1/market/number-of-files::site.json` | [docs](https://build.envato.com/api/#market_getNumberOfFiles) |
| [Get ThemeForest New Files](actions/get-themeforest-new-files.md) | `GET /v1/market/new-files::site,:category.json` | [docs](https://build.envato.com/api/#market_getNewFiles) |
| [Get ThemeForest Popular Items](actions/get-themeforest-popular-items.md) | `GET /v1/market/popular::site.json` | [docs](https://build.envato.com/api/#market_getPopular) |
| [Get ThemeForest Random New Files](actions/get-themeforest-random-new-files.md) | `GET /v1/market/random-new-files::site.json` | [docs](https://build.envato.com/api/#market_getRandomNewFiles) |
| [Get User Badges](actions/get-user-badges.md) | `GET /v1/market/user-badges::username.json` | [docs](https://build.envato.com/api/#market_getUserBadges) |
| [Get User Items By Site](actions/get-user-items-by-site.md) | `GET /v1/market/user-items-by-site::username.json` | [docs](https://build.envato.com/api/#market_getUserItemsBySite) |
| [Get User Profile](actions/get-user-profile.md) | `GET /v1/market/user::username.json` | [docs](https://build.envato.com/api/#market_getUser) |
| [List Author Sales](actions/list-author-sales.md) | `GET /v3/market/author/sales` | [docs](https://build.envato.com/api/#market_0_getAuthorSales) |
| [List Purchases](actions/list-purchases.md) | `GET /v3/market/buyer/list-purchases` | [docs](https://build.envato.com/api/#market_0_getBuyerListPurchases) |
| [Search Item Comments](actions/search-item-comments.md) | `GET /v1/discovery/search/search/comment` | [docs](https://build.envato.com/api/#search_getSearchComment) |
| [Search ThemeForest Items](actions/search-themeforest-items.md) | `GET /v1/discovery/search/search/item` | [docs](https://build.envato.com/api/#search_getSearchItem) |
