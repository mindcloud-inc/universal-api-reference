# AppFollow: Native API Reference

A consolidated summary of AppFollow's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.appfollow.io/reference/overview
- **API base URL:** `https://api.appfollow.io`

## Authentication

### API Key

Connect AppFollow with an API token from the AppFollow API Dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-AppFollow-API-Token: <apiKey>
```

[Official authentication documentation](https://docs.api.appfollow.io/reference/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `reviews.list`. The total page count is read from `reviews.page.total`. The current page number is read from `reviews.page.current`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Keyword Suggestions](actions/get-keyword-suggestions.md) | `GET /api/v2/aso/suggests` | [docs](https://docs.api.appfollow.io/reference/aso_keyword_research_api_v2_aso_suggests_get-1) |
| [Get Ratings History](actions/get-ratings-history.md) | `GET /api/v2/meta/ratings/history` | [docs](https://docs.api.appfollow.io/reference/ratings_history_api_v2_meta_ratings_history_get) |
| [Get Review Rating Stats](actions/get-review-rating-stats.md) | `GET /api/v2/reviews/stats/ratings` | [docs](https://docs.api.appfollow.io/reference/stat_reviews_rating_api_v2_reviews_stats_ratings_get-1) |
| [Get Review Reply Counts](actions/get-review-reply-counts.md) | `GET /api/v2/reviews/stats/replies/count` | [docs](https://docs.api.appfollow.io/reference/replies_statistics_api_v2_reviews_stats_replies_count_get-1) |
| [Get Review Reply Speed](actions/get-review-reply-speed.md) | `GET /api/v2/reviews/stats/replies/speed` | [docs](https://docs.api.appfollow.io/reference/stat_replies_speed_api_v2_reviews_stats_replies_speed_get-1) |
| [Get Review Reply Stats](actions/get-review-reply-stats.md) | `GET /api/v2/reviews/stats/replies` | [docs](https://docs.api.appfollow.io/reference/stat_reviews_replies_api_v2_reviews_stats_replies_get-1) |
| [Get Review Stats](actions/get-review-stats.md) | `GET /api/v2/reviews/stats` | [docs](https://docs.api.appfollow.io/reference/stat_reviews_api_v2_reviews_stats_get-1) |
| [Get Review Summary](actions/get-review-summary.md) | `GET /api/v2/reviews/summary` | [docs](https://docs.api.appfollow.io/reference/reviews_summary_api_v2_reviews_summary_get-1) |
| [List App Collections](actions/list-app-collections.md) | `GET /api/v2/account/apps` | [docs](https://docs.api.appfollow.io/reference/app_collections_list_api_v2_account_apps_get-1) |
| [List Collection Apps](actions/list-collection-apps.md) | `GET /api/v2/account/apps/app` | [docs](https://docs.api.appfollow.io/reference/list_of_apps_from_the_collection_api_v2_account_apps_app_get-1) |
| [List Featured Reviews](actions/list-featured-reviews.md) | `GET /api/v2/reviews/featured` | [docs](https://docs.api.appfollow.io/reference/featured_reviews_api_v2_reviews_featured_get-1) |
| [List Keywords](actions/list-keywords.md) | `GET /api/v2/aso/keywords` | [docs](https://docs.api.appfollow.io/reference/keywords_api_v2_aso_keywords_get-1) |
| [List New Versions](actions/list-new-versions.md) | `GET /api/v2/meta/versions/whatsnew` | [docs](https://docs.api.appfollow.io/reference/what_s_new__new_versions__api_v2_meta_versions_whatsnew_get-1) |
| [List Rankings](actions/list-rankings.md) | `GET /api/v2/meta/rankings` | [docs](https://docs.api.appfollow.io/reference/rankings_api_v2_meta_rankings_get-1) |
| [List Reviews](actions/list-reviews.md) | `GET /api/v2/reviews` | [docs](https://docs.api.appfollow.io/reference/reviews_api_v2_reviews_get-1) |
| [List Top Charts](actions/list-top-charts.md) | `GET /api/v2/charts/topcharts` | [docs](https://docs.api.appfollow.io/reference/public_top_charts_api_v2_charts_topcharts_get-1) |
| [List Users](actions/list-users.md) | `GET /api/v2/account/users` | [docs](https://docs.api.appfollow.io/reference/users_list_api_v2_account_users_get-1) |
| [List Versions](actions/list-versions.md) | `GET /api/v2/meta/versions` | [docs](https://docs.api.appfollow.io/reference/versions__any_changes_including_meta_data__api_v2_meta_versions_get-1) |
| [Search ASO](actions/search-aso.md) | `GET /api/v2/aso/search` | [docs](https://docs.api.appfollow.io/reference/aso_search_api_v2_aso_search_get-1) |
