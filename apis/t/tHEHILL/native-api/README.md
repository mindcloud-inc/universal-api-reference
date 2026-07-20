# THE HILL: Native API Reference

A consolidated summary of THE HILL's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.wordpress.org/rest-api/
- **API base URL:** `https://thehill.com/wp-json/`

## Authentication

### Public Read

Read public WordPress content without authentication.

This API does not require request authentication.

[Official authentication documentation](https://developer.wordpress.org/rest-api/)

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | `GET /wp/v2/categories/{id}` | [docs](https://developer.wordpress.org/rest-api/reference/categories/) |
| [Get Media](actions/get-media.md) | `GET /wp/v2/media/{id}` | [docs](https://developer.wordpress.org/rest-api/reference/media/) |
| [Get Page](actions/get-page.md) | `GET /wp/v2/pages/{id}` | [docs](https://developer.wordpress.org/rest-api/reference/pages/) |
| [Get Post](actions/get-post.md) | `GET /wp/v2/posts/{id}` | [docs](https://developer.wordpress.org/rest-api/reference/posts/) |
| [Get Tag](actions/get-tag.md) | `GET /wp/v2/tags/{id}` | [docs](https://developer.wordpress.org/rest-api/reference/tags/) |
| [List Alerts](actions/list-alerts.md) | `GET /wp/v2/alerts` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Categories](actions/list-categories.md) | `GET /wp/v2/categories` | [docs](https://developer.wordpress.org/rest-api/reference/categories/) |
| [List City Tags](actions/list-city-tags.md) | `GET /wp/v2/city_tags` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Company Tags](actions/list-company-tags.md) | `GET /wp/v2/company_tags` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Country Tags](actions/list-country-tags.md) | `GET /wp/v2/country_tags` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Email Newsletters](actions/list-email-newsletters.md) | `GET /wp/v2/email_newsletter` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Events](actions/list-events.md) | `GET /wp/v2/event` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Events Facts Tags](actions/list-events-facts-tags.md) | `GET /wp/v2/events_facts_tags` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Feed Posts](actions/list-feed-posts.md) | `GET /wp/v2/feed-posts` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Future America Posts](actions/list-future-america-posts.md) | `GET /wp/v2/future_america_post` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Galleries](actions/list-galleries.md) | `GET /wp/v2/galleries` | [docs](https://developer.wordpress.org/rest-api/) |
| [List HillTV Posts](actions/list-hilltv-posts.md) | `GET /wp/v2/hilltv_post` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Link Posts](actions/list-link-posts.md) | `GET /wp/v2/link-posts` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Media](actions/list-media.md) | `GET /wp/v2/media` | [docs](https://developer.wordpress.org/rest-api/reference/media/) |
| [List Navigation](actions/list-navigation.md) | `GET /wp/v2/navigation` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Newsletter Posts](actions/list-newsletter-posts.md) | `GET /wp/v2/newsletter_post` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Nota](actions/list-nota.md) | `GET /wp/v2/nota` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Pages](actions/list-pages.md) | `GET /wp/v2/pages` | [docs](https://developer.wordpress.org/rest-api/reference/pages/) |
| [List Posts](actions/list-posts.md) | `GET /wp/v2/posts` | [docs](https://developer.wordpress.org/rest-api/reference/posts/) |
| [List Statuses](actions/list-statuses.md) | `GET /wp/v2/statuses` | [docs](https://developer.wordpress.org/rest-api/reference/statuses/) |
| [List Tags](actions/list-tags.md) | `GET /wp/v2/tags` | [docs](https://developer.wordpress.org/rest-api/reference/tags/) |
| [List Vertical Posts](actions/list-vertical-posts.md) | `GET /wp/v2/vertical_post` | [docs](https://developer.wordpress.org/rest-api/) |
| [List Videos](actions/list-videos.md) | `GET /wp/v2/video` | [docs](https://developer.wordpress.org/rest-api/) |
| [RSS Feed](actions/rss-feed.md) | `GET /feed/` | [docs](https://thehill.com/feed/) |
| [Search Content](actions/search-content.md) | `GET /wp/v2/search` | [docs](https://developer.wordpress.org/rest-api/reference/search-results/) |
