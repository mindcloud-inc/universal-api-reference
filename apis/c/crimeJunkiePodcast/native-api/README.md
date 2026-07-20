# Crime Junkie Podcast: Native API Reference

A consolidated summary of Crime Junkie Podcast's API configuration and 58 documented operations, with links to official documentation.

- **Official docs:** https://crimejunkiepodcast.com/wp-json/
- **API base URL:** `https://crimejunkiepodcast.com`

## Authentication

### No Authentication

The official Crime Junkie Podcast RSS feed is public and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://crimejunkiepodcast.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9, */*;q=0.8` |
| `User-Agent` | `MindCloud/1.0 (apps@mindcloud.co)` |

Responses from this API use XML.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (58 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Attachment Category](actions/get-attachment-category.md) | `GET /wp-json/wp/v2/attachment-category/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/attachment-category) |
| [Get Author](actions/get-author.md) | `GET /wp-json/wp/v2/users/:id` | [docs](https://developer.wordpress.org/rest-api/reference/users/) |
| [Get Block](actions/get-block.md) | `GET /wp-json/wp/v2/blocks/:id` | [docs](https://developer.wordpress.org/rest-api/reference/blocks/) |
| [Get Category](actions/get-category.md) | `GET /wp-json/wp/v2/categories/:id` | [docs](https://developer.wordpress.org/rest-api/reference/categories/) |
| [Get Comment](actions/get-comment.md) | `GET /wp-json/wp/v2/comments/:id` | [docs](https://developer.wordpress.org/rest-api/reference/comments/) |
| [Get Content Type](actions/get-content-type.md) | `GET /wp-json/wp/v2/types/:type` | [docs](https://developer.wordpress.org/rest-api/reference/post-types/) |
| [Get Dipi Content Category](actions/get-dipi-content-category.md) | `GET /wp-json/wp/v2/dipi_cpt_category/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/dipi_cpt_category) |
| [Get Dipi Media Category](actions/get-dipi-media-category.md) | `GET /wp-json/wp/v2/dipi_media_category/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/dipi_media_category) |
| [Get Fan Club Episode](actions/get-fan-club-episode.md) | `GET /wp-json/wp/v2/fan-club/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/fan-club) |
| [Get Fan Club Tier](actions/get-fan-club-tier.md) | `GET /wp-json/wp/v2/fan_club_tier/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/fan_club_tier) |
| [Get Good Tag](actions/get-good-tag.md) | `GET /wp-json/wp/v2/good/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/good) |
| [Get Media](actions/get-media.md) | `GET /wp-json/wp/v2/media/:id` | [docs](https://developer.wordpress.org/rest-api/reference/media/) |
| [Get Navigation Menu](actions/get-navigation-menu.md) | `GET /wp-json/wp/v2/navigation/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/navigation) |
| [Get OEmbed Embed](actions/get-oembed-embed.md) | `GET /wp-json/oembed/1.0/embed` | [docs](https://crimejunkiepodcast.com/wp-json/oembed/1.0/embed) |
| [Get OEmbed Namespace Info](actions/get-oembed-namespace-info.md) | `GET /wp-json/oembed/1.0` | [docs](https://crimejunkiepodcast.com/wp-json/oembed/1.0) |
| [Get Page](actions/get-page.md) | `GET /wp-json/wp/v2/pages/:id` | [docs](https://developer.wordpress.org/rest-api/reference/pages/) |
| [Get Pattern Category](actions/get-pattern-category.md) | `GET /wp-json/wp/v2/wp_pattern_category/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/wp_pattern_category) |
| [Get Popup Maker](actions/get-popup-maker.md) | `GET /wp-json/wp/v2/dipi_popup_maker/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/dipi_popup_maker) |
| [Get Post](actions/get-post.md) | `GET /wp-json/wp/v2/posts/:id` | [docs](https://developer.wordpress.org/rest-api/reference/posts/) |
| [Get Project](actions/get-project.md) | `GET /wp-json/wp/v2/project/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/project) |
| [Get Project Category](actions/get-project-category.md) | `GET /wp-json/wp/v2/project_category/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/project_category) |
| [Get Project Tag](actions/get-project-tag.md) | `GET /wp-json/wp/v2/project_tag/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/project_tag) |
| [Get Pruppet](actions/get-pruppet.md) | `GET /wp-json/wp/v2/pruppet-of-the-month/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/pruppet-of-the-month) |
| [Get Pruppet Category](actions/get-pruppet-category.md) | `GET /wp-json/wp/v2/pruppet_category/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/pruppet_category) |
| [Get Site API Root](actions/get-site-api-root.md) | `GET /wp-json/` | [docs](https://developer.wordpress.org/rest-api/) |
| [Get Status](actions/get-status.md) | `GET /wp-json/wp/v2/statuses/:status` | [docs](https://developer.wordpress.org/rest-api/reference/post-statuses/) |
| [Get Tag](actions/get-tag.md) | `GET /wp-json/wp/v2/tags/:id` | [docs](https://developer.wordpress.org/rest-api/reference/tags/) |
| [Get Taxonomy](actions/get-taxonomy.md) | `GET /wp-json/wp/v2/taxonomies/:taxonomy` | [docs](https://developer.wordpress.org/rest-api/reference/taxonomies/) |
| [Get The Good](actions/get-the-good.md) | `GET /wp-json/wp/v2/the-good/:id` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/the-good) |
| [Get WordPress Namespace Info](actions/get-wordpress-namespace-info.md) | `GET /wp-json/wp/v2` | [docs](https://developer.wordpress.org/rest-api/reference/) |
| [List Attachment Categories](actions/list-attachment-categories.md) | `GET /wp-json/wp/v2/attachment-category` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/attachment-category) |
| [List Authors](actions/list-authors.md) | `GET /wp-json/wp/v2/users` | [docs](https://developer.wordpress.org/rest-api/reference/users/) |
| [List Blocks](actions/list-blocks.md) | `GET /wp-json/wp/v2/blocks` | [docs](https://developer.wordpress.org/rest-api/reference/blocks/) |
| [List Categories](actions/list-categories.md) | `GET /wp-json/wp/v2/categories` | [docs](https://developer.wordpress.org/rest-api/reference/categories/) |
| [List Comments](actions/list-comments.md) | `GET /wp-json/wp/v2/comments` | [docs](https://developer.wordpress.org/rest-api/reference/comments/) |
| [List Content Types](actions/list-content-types.md) | `GET /wp-json/wp/v2/types` | [docs](https://developer.wordpress.org/rest-api/reference/post-types/) |
| [List Dipi Content Categories](actions/list-dipi-content-categories.md) | `GET /wp-json/wp/v2/dipi_cpt_category` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/dipi_cpt_category) |
| [List Dipi Media Categories](actions/list-dipi-media-categories.md) | `GET /wp-json/wp/v2/dipi_media_category` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/dipi_media_category) |
| [List Fan Club Episodes](actions/list-fan-club-episodes.md) | `GET /wp-json/wp/v2/fan-club` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/fan-club) |
| [List Fan Club Tiers](actions/list-fan-club-tiers.md) | `GET /wp-json/wp/v2/fan_club_tier` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/fan_club_tier) |
| [List Good Tags](actions/list-good-tags.md) | `GET /wp-json/wp/v2/good` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/good) |
| [List Media](actions/list-media.md) | `GET /wp-json/wp/v2/media` | [docs](https://developer.wordpress.org/rest-api/reference/media/) |
| [List Navigation Menus](actions/list-navigation-menus.md) | `GET /wp-json/wp/v2/navigation` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/navigation) |
| [List Pages](actions/list-pages.md) | `GET /wp-json/wp/v2/pages` | [docs](https://developer.wordpress.org/rest-api/reference/pages/) |
| [List Pattern Categories](actions/list-pattern-categories.md) | `GET /wp-json/wp/v2/wp_pattern_category` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/wp_pattern_category) |
| [List Popup Makers](actions/list-popup-makers.md) | `GET /wp-json/wp/v2/dipi_popup_maker` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/dipi_popup_maker) |
| [List Posts](actions/list-posts.md) | `GET /wp-json/wp/v2/posts` | [docs](https://developer.wordpress.org/rest-api/reference/posts/) |
| [List Project Categories](actions/list-project-categories.md) | `GET /wp-json/wp/v2/project_category` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/project_category) |
| [List Project Tags](actions/list-project-tags.md) | `GET /wp-json/wp/v2/project_tag` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/project_tag) |
| [List Projects](actions/list-projects.md) | `GET /wp-json/wp/v2/project` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/project) |
| [List Pruppet Categories](actions/list-pruppet-categories.md) | `GET /wp-json/wp/v2/pruppet_category` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/pruppet_category) |
| [List Pruppets](actions/list-pruppets.md) | `GET /wp-json/wp/v2/pruppet-of-the-month` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/pruppet-of-the-month) |
| [List Recent Episodes](actions/list-recent-episodes.md) | `GET /feed/` | [docs](https://crimejunkiepodcast.com/feed/) |
| [List Statuses](actions/list-statuses.md) | `GET /wp-json/wp/v2/statuses` | [docs](https://developer.wordpress.org/rest-api/reference/post-statuses/) |
| [List Tags](actions/list-tags.md) | `GET /wp-json/wp/v2/tags` | [docs](https://developer.wordpress.org/rest-api/reference/tags/) |
| [List Taxonomies](actions/list-taxonomies.md) | `GET /wp-json/wp/v2/taxonomies` | [docs](https://developer.wordpress.org/rest-api/reference/taxonomies/) |
| [List The Goods](actions/list-the-goods.md) | `GET /wp-json/wp/v2/the-good` | [docs](https://crimejunkiepodcast.com/wp-json/wp/v2/the-good) |
| [Search Content](actions/search-content.md) | `GET /wp-json/wp/v2/search` | [docs](https://developer.wordpress.org/rest-api/reference/search-results/) |
