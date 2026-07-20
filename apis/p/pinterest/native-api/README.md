# Pinterest: Native API Reference

A consolidated summary of Pinterest's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://developers.pinterest.com/docs/api/v5/introduction/
- **OpenAPI specification:** https://raw.githubusercontent.com/pinterest/api-description/main/v5/openapi.json
- **API base URL:** `https://api.pinterest.com/v5`

## Authentication

### OAuth 2.0

Pinterest OAuth 2.0 authorization-code authentication for user, board, pin, catalog, and ads API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.pinterest.com/oauth/ to approve access.
2. Exchange the returned authorization code with a POST request to https://api.pinterest.com/v5/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ads:read ads:write billing:read billing:write biz_access:read biz_access:write boards:read boards:read_secret boards:write boards:write_secret catalogs:read catalogs:write pins:read pins:read_secret pins:write pins:write_secret user_accounts:read user_accounts:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.pinterest.com/v5/oauth/token.

[Official authentication documentation](https://developers.pinterest.com/docs/api/v5/introduction/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–250). Use `bookmark` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | `POST boards` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/boards/create) |
| [Create Board Section](actions/create-board-section.md) | `POST boards/:boardId/sections` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/board_sections/create) |
| [Create Catalog](actions/create-catalog.md) | `POST catalogs` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/catalogs/create) |
| [Create Pin](actions/create-pin.md) | `POST pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/pins/create) |
| [Delete Board](actions/delete-board.md) | `DELETE boards/:boardId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/boards/delete) |
| [Delete Board Section](actions/delete-board-section.md) | `DELETE boards/:boardId/sections/:sectionId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/board_sections/delete) |
| [Delete Pin](actions/delete-pin.md) | `DELETE pins/:pinId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/pins/delete) |
| [Get Ad Account](actions/get-ad-account.md) | `GET ad_accounts/:adAccountId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/ad_accounts/get) |
| [Get Board](actions/get-board.md) | `GET boards/:boardId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/boards/get) |
| [Get Catalog Item Batch Status](actions/get-catalog-item-batch-status.md) | `GET catalogs/items/batch/:batchId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/items_batch/get) |
| [Get Catalog Items](actions/get-catalog-items.md) | `POST catalogs/items` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/items/post) |
| [Get Media Upload](actions/get-media-upload.md) | `GET media/:mediaId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/media/get) |
| [Get Pin](actions/get-pin.md) | `GET pins/:pinId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/pins/get) |
| [Get Product Group](actions/get-product-group.md) | `GET catalogs/product_groups/:productGroupId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/catalogs_product_groups/get) |
| [Get Top Pins Analytics](actions/get-top-pins-analytics.md) | `GET user_account/analytics/top_pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/user_account/analytics/top_pins) |
| [Get Top Video Pins Analytics](actions/get-top-video-pins-analytics.md) | `GET user_account/analytics/top_video_pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/user_account/analytics/top_video_pins) |
| [Get User Account](actions/get-user-account.md) | `GET user_account` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/user_account/get) |
| [Get User Account Analytics](actions/get-user-account-analytics.md) | `GET user_account/analytics` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/user_account/analytics) |
| [List Ad Accounts](actions/list-ad-accounts.md) | `GET ad_accounts` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/ad_accounts/list) |
| [List Ad Groups](actions/list-ad-groups.md) | `GET ad_accounts/:adAccountId/ad_groups` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/ad_groups/list) |
| [List Ads](actions/list-ads.md) | `GET ad_accounts/:adAccountId/ads` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/ads/list) |
| [List Board Pins](actions/list-board-pins.md) | `GET boards/:boardId/pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/boards/list_pins) |
| [List Board Section Pins](actions/list-board-section-pins.md) | `GET boards/:boardId/sections/:sectionId/pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/board_sections/list_pins) |
| [List Board Sections](actions/list-board-sections.md) | `GET boards/:boardId/sections` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/board_sections/list) |
| [List Boards](actions/list-boards.md) | `GET boards` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/boards/list) |
| [List Campaigns](actions/list-campaigns.md) | `GET ad_accounts/:adAccountId/campaigns` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/campaigns/list) |
| [List Catalogs](actions/list-catalogs.md) | `GET catalogs` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/catalogs/list) |
| [List Followers](actions/list-followers.md) | `GET user_account/followers` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/followers/list) |
| [List Pins](actions/list-pins.md) | `GET pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/pins/list) |
| [List Product Groups](actions/list-product-groups.md) | `GET catalogs/product_groups` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/catalogs_product_groups/list) |
| [List Products By Product Group](actions/list-products-by-product-group.md) | `GET catalogs/product_groups/:productGroupId/products` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/catalogs_product_group_pins/list) |
| [Operate On Product Pins](actions/operate-on-product-pins.md) | `POST catalogs/items/batch` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/items_batch/post) |
| [Register Media Upload](actions/register-media-upload.md) | `POST media` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/media/create) |
| [Save Pin](actions/save-pin.md) | `POST pins/:pinId/save` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/pins/save) |
| [Search Boards](actions/search-boards.md) | `GET search/boards` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/search_user_boards/get) |
| [Search Pins](actions/search-pins.md) | `GET search/pins` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/search_user_pins/list) |
| [Update Board](actions/update-board.md) | `PATCH boards/:boardId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/boards/update) |
| [Update Board Section](actions/update-board-section.md) | `PATCH boards/:boardId/sections/:sectionId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/board_sections/update) |
| [Update Pin](actions/update-pin.md) | `PATCH pins/:pinId` | [docs](https://developers.pinterest.com/docs/api/v5/#operation/pins/update) |
