# Lex Fridman Podcast: Native API Reference

A consolidated summary of Lex Fridman Podcast's API configuration and 34 documented operations.

- **API base URL:** `https://lexfridman.com`

## Authentication

### No Authentication

Public read-only endpoints on lexfridman.com require no credentials.

This API does not require request authentication.

[Official authentication documentation](https://lexfridman.com/wp-json/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | `GET /wp-json/wp/v2/categories/:id` | [docs](https://lexfridman.com/wp-json/) |
| [Get Content Type](actions/get-content-type.md) | `GET /wp-json/wp/v2/types/:type` | [docs](https://lexfridman.com/wp-json/) |
| [Get Media](actions/get-media.md) | `GET /wp-json/wp/v2/media/:id` | [docs](https://lexfridman.com/wp-json/) |
| [Get OEmbed Embed](actions/get-oembed-embed.md) | `GET /wp-json/oembed/1.0/embed` | [docs](https://lexfridman.com/wp-json/) |
| [Get OEmbed Namespace Info](actions/get-oembed-namespace-info.md) | `GET /wp-json/oembed/1.0` | [docs](https://lexfridman.com/wp-json/) |
| [Get Page](actions/get-page.md) | `GET /wp-json/wp/v2/pages/:id` | [docs](https://lexfridman.com/wp-json/) |
| [Get Post](actions/get-post.md) | `GET /wp-json/wp/v2/posts/:id` | [docs](https://lexfridman.com/wp-json/) |
| [Get Site API Root](actions/get-site-api-root.md) | `GET /wp-json/` | [docs](https://lexfridman.com/wp-json/) |
| [Get Status](actions/get-status.md) | `GET /wp-json/wp/v2/statuses/:status` | [docs](https://lexfridman.com/wp-json/) |
| [Get Taxonomy](actions/get-taxonomy.md) | `GET /wp-json/wp/v2/taxonomies/:taxonomy` | [docs](https://lexfridman.com/wp-json/) |
| [Get WordPress Namespace Info](actions/get-wordpress-namespace-info.md) | `GET /wp-json/wp/v2` | [docs](https://lexfridman.com/wp-json/) |
| [List Blocks](actions/list-blocks.md) | `GET /wp-json/wp/v2/blocks` | [docs](https://lexfridman.com/wp-json/) |
| [List Categories](actions/list-categories.md) | `GET /wp-json/wp/v2/categories` | [docs](https://lexfridman.com/wp-json/) |
| [List Comments](actions/list-comments.md) | `GET /wp-json/wp/v2/comments` | [docs](https://lexfridman.com/wp-json/) |
| [List Content Types](actions/list-content-types.md) | `GET /wp-json/wp/v2/types` | [docs](https://lexfridman.com/wp-json/) |
| [List Media](actions/list-media.md) | `GET /wp-json/wp/v2/media` | [docs](https://lexfridman.com/wp-json/) |
| [List Navigation Menus](actions/list-navigation-menus.md) | `GET /wp-json/wp/v2/navigation` | [docs](https://lexfridman.com/wp-json/) |
| [List Pages](actions/list-pages.md) | `GET /wp-json/wp/v2/pages` | [docs](https://lexfridman.com/wp-json/) |
| [List Pattern Categories](actions/list-pattern-categories.md) | `GET /wp-json/wp/v2/wp_pattern_category` | [docs](https://lexfridman.com/wp-json/) |
| [List Posts](actions/list-posts.md) | `GET /wp-json/wp/v2/posts` | [docs](https://lexfridman.com/wp-json/) |
| [List Posts By Author](actions/list-posts-by-author.md) | `GET /wp-json/wp/v2/posts` | [docs](https://lexfridman.com/wp-json/) |
| [List Posts By Category](actions/list-posts-by-category.md) | `GET /wp-json/wp/v2/posts` | [docs](https://lexfridman.com/wp-json/) |
| [List Statuses](actions/list-statuses.md) | `GET /wp-json/wp/v2/statuses` | [docs](https://lexfridman.com/wp-json/) |
| [List Tags](actions/list-tags.md) | `GET /wp-json/wp/v2/tags` | [docs](https://lexfridman.com/wp-json/) |
| [List Taxonomies](actions/list-taxonomies.md) | `GET /wp-json/wp/v2/taxonomies` | [docs](https://lexfridman.com/wp-json/) |
| [List Users](actions/list-users.md) | `GET /wp-json/wp/v2/users` | [docs](https://lexfridman.com/wp-json/) |
| [Search Categories](actions/search-categories.md) | `GET /wp-json/wp/v2/categories` | [docs](https://lexfridman.com/wp-json/) |
| [Search Content](actions/search-content.md) | `GET /wp-json/wp/v2/search` | [docs](https://lexfridman.com/wp-json/) |
| [Search Media](actions/search-media.md) | `GET /wp-json/wp/v2/media` | [docs](https://lexfridman.com/wp-json/) |
| [Search Pages](actions/search-pages.md) | `GET /wp-json/wp/v2/pages` | [docs](https://lexfridman.com/wp-json/) |
| [Search Posts](actions/search-posts.md) | `GET /wp-json/wp/v2/posts` | [docs](https://lexfridman.com/wp-json/) |
| [Search Tags](actions/search-tags.md) | `GET /wp-json/wp/v2/tags` | [docs](https://lexfridman.com/wp-json/) |
| [Search Terms](actions/search-terms.md) | `GET /wp-json/wp/v2/search` | [docs](https://lexfridman.com/wp-json/) |
| [Search Users](actions/search-users.md) | `GET /wp-json/wp/v2/users` | [docs](https://lexfridman.com/wp-json/) |
