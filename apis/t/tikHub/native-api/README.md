# TikHub: Native API Reference

A consolidated summary of TikHub's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.tikhub.io/
- **OpenAPI specification:** https://api.tikhub.io/openapi.json
- **API base URL:** `https://api.tikhub.io`

## Authentication

### API Key

Use a TikHub API token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.tikhub.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Stop after 3 attempts.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Endpoint Price](actions/calculate-endpoint-price.md) | `GET /api/v1/tikhub/user/calculate_price` | [docs](https://api.tikhub.io/#/TikHub-User-API/calculate_price_api_v1_tikhub_user_calculate_price_get) |
| [Get All Endpoints Info](actions/get-all-endpoints-info.md) | `GET /api/v1/tikhub/user/get_all_endpoints_info` | [docs](https://api.tikhub.io/#/TikHub-User-API/get_all_endpoints_info_api_v1_tikhub_user_get_all_endpoints_info_get) |
| [Get Endpoint Info](actions/get-endpoint-info.md) | `GET /api/v1/tikhub/user/get_endpoint_info` | [docs](https://api.tikhub.io/#/TikHub-User-API/get_endpoint_info_api_v1_tikhub_user_get_endpoint_info_get) |
| [Get General Search Results](actions/get-general-search-results.md) | `GET /api/v1/tiktok/app/v3/fetch_general_search_result` | [docs](https://api.tikhub.io/#/TikTok-App-V3-API/fetch_general_search_result_api_v1_tiktok_app_v3_fetch_general_search_result_get) |
| [Get Hot Selling Products](actions/get-hot-selling-products.md) | `GET /api/v1/tiktok/shop/web/fetch_hot_selling_products_list` | [docs](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_hot_selling_products_list_api_v1_tiktok_shop_web_fetch_hot_selling_products_list_get) |
| [Get Product Categories](actions/get-product-categories.md) | `GET /api/v1/tiktok/shop/web/fetch_products_category_list` | [docs](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_products_category_list_api_v1_tiktok_shop_web_fetch_products_category_list_get) |
| [Get Product Detail](actions/get-product-detail.md) | `GET /api/v1/tiktok/shop/web/fetch_product_detail` | [docs](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_product_detail_api_v1_tiktok_shop_web_fetch_product_detail_get) |
| [Get Product Search Suggestions](actions/get-product-search-suggestions.md) | `GET /api/v1/tiktok/shop/web/fetch_search_word_suggestion` | [docs](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_search_word_suggestion_api_v1_tiktok_shop_web_fetch_search_word_suggestion_get) |
| [Get Search Keyword Suggestions](actions/get-search-keyword-suggestions.md) | `GET /api/v1/tiktok/web/fetch_search_keyword_suggest` | [docs](https://api.tikhub.io/#/TikTok-Web-API/fetch_search_keyword_suggest_api_v1_tiktok_web_fetch_search_keyword_suggest_get) |
| [Get Seller Products](actions/get-seller-products.md) | `GET /api/v1/tiktok/shop/web/fetch_seller_products_list` | [docs](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_seller_products_list_api_v1_tiktok_shop_web_fetch_seller_products_list_get) |
| [Get Single Video](actions/get-single-video.md) | `GET /api/v1/tiktok/app/v3/fetch_one_video` | [docs](https://api.tikhub.io/#/TikTok-App-V3-API/fetch_one_video_api_v1_tiktok_app_v3_fetch_one_video_get) |
| [Get Tiered Discount Info](actions/get-tiered-discount-info.md) | `GET /api/v1/tikhub/user/get_tiered_discount_info` | [docs](https://api.tikhub.io/#/TikHub-User-API/get_tiered_discount_info_api_v1_tikhub_user_get_tiered_discount_info_get) |
| [Get TikHub User Info](actions/get-tik-hub-user-info.md) | `GET /api/v1/tikhub/user/get_user_info` | [docs](https://api.tikhub.io/#/TikHub-User-API/get_user_info_api_v1_tikhub_user_get_user_info_get) |
| [Get Trending Search Keywords](actions/get-trending-search-keywords.md) | `GET /api/v1/tiktok/web/fetch_trending_searchwords` | [docs](https://api.tikhub.io/#/TikTok-Web-API/fetch_trending_searchwords_api_v1_tiktok_web_fetch_trending_searchwords_get) |
| [Get User Daily Usage](actions/get-user-daily-usage.md) | `GET /api/v1/tikhub/user/get_user_daily_usage` | [docs](https://api.tikhub.io/#/TikHub-User-API/get_user_daily_usage_api_v1_tikhub_user_get_user_daily_usage_get) |
| [Get User IDs by Username](actions/get-user-ids-by-username.md) | `GET /api/v1/tiktok/app/v3/get_user_id_and_sec_user_id_by_username` | [docs](https://api.tikhub.io/#/TikTok-App-V3-API/get_user_id_and_sec_user_id_by_username_api_v1_tiktok_app_v3_get_user_id_and_sec_user_id_by_username_get) |
| [Get User Posts](actions/get-user-posts.md) | `GET /api/v1/tiktok/web/fetch_user_post` | [docs](https://api.tikhub.io/#/TikTok-Web-API/fetch_user_post_api_v1_tiktok_web_fetch_user_post_get) |
| [Get User Profile](actions/get-user-profile.md) | `GET /api/v1/tiktok/web/fetch_user_profile` | [docs](https://api.tikhub.io/#/TikTok-Web-API/fetch_user_profile_api_v1_tiktok_web_fetch_user_profile_get) |
| [Get User Profile by Identifier](actions/get-user-profile-by-identifier.md) | `GET /api/v1/tiktok/app/v3/handler_user_profile` | [docs](https://api.tikhub.io/#/TikTok-App-V3-API/handler_user_profile_api_v1_tiktok_app_v3_handler_user_profile_get) |
| [Get Video Comments](actions/get-video-comments.md) | `GET /api/v1/tiktok/app/v3/fetch_video_comments` | [docs](https://api.tikhub.io/#/TikTok-App-V3-API/fetch_video_comments_api_v1_tiktok_app_v3_fetch_video_comments_get) |
| [Get Video Detail](actions/get-video-detail.md) | `GET /api/v1/tiktok/web/fetch_post_detail` | [docs](https://api.tikhub.io/#/TikTok-Web-API/fetch_post_detail_api_v1_tiktok_web_fetch_post_detail_get) |
| [Get Video Search Results](actions/get-video-search-results.md) | `GET /api/v1/tiktok/app/v3/fetch_video_search_result` | [docs](https://api.tikhub.io/#/TikTok-App-V3-API/fetch_video_search_result_api_v1_tiktok_app_v3_fetch_video_search_result_get) |
| [Search Products](actions/search-products.md) | `GET /api/v1/tiktok/shop/web/fetch_search_products_list` | [docs](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_search_products_list_api_v1_tiktok_shop_web_fetch_search_products_list_get) |
| [Search Videos](actions/search-videos.md) | `GET /api/v1/tiktok/web/fetch_search_video` | [docs](https://api.tikhub.io/#/TikTok-Web-API/fetch_search_video_api_v1_tiktok_web_fetch_search_video_get) |
