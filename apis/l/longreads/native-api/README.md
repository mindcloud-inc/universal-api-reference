# Longreads: Native API Reference

A consolidated summary of Longreads's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://longreads.com/wp-json/
- **API base URL:** `https://longreads.com/wp-json`

## Authentication

### Public Access

No authentication required

This API does not require request authentication.

[Official authentication documentation](https://longreads.com/wp-json/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | `GET /wp/v2/categories/{id}` | [docs](https://longreads.com/wp-json/wp/v2/categories) |
| [Get Coauthor](actions/get-coauthor.md) | `GET /coauthors/v1/coauthors/{user_nicename}` | [docs](https://longreads.com/wp-json/coauthors/v1/coauthors/adminnewspack) |
| [Get Guest Author](actions/get-guest-author.md) | `GET /wp/v2/guest-author/{id}` | [docs](https://longreads.com/wp-json/wp/v2/guest-author) |
| [Get Longreads Recommendations](actions/get-longreads-recommendations.md) | `GET /longreads/v1/recommendations` | [docs](https://longreads.com/wp-json/longreads/v1/recommendations) |
| [Get Media](actions/get-media.md) | `GET /wp/v2/media/{id}` | [docs](https://longreads.com/wp-json/wp/v2/media) |
| [Get OEmbed Metadata](actions/get-oembed-metadata.md) | `GET /oembed/1.0/embed` | [docs](https://longreads.com/wp-json/oembed/1.0/embed) |
| [Get Page](actions/get-page.md) | `GET /wp/v2/pages/{id}` | [docs](https://longreads.com/wp-json/wp/v2/pages) |
| [Get Post](actions/get-post.md) | `GET /wp/v2/posts/{id}` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [Get Post Type](actions/get-post-type.md) | `GET /wp/v2/types/{type}` | [docs](https://longreads.com/wp-json/wp/v2/types) |
| [Get Post Type Index](actions/get-post-type-index.md) | `GET /wp/v2/types` | [docs](https://longreads.com/wp-json/wp/v2/types) |
| [Get Tag](actions/get-tag.md) | `GET /wp/v2/tags/{id}` | [docs](https://longreads.com/wp-json/wp/v2/tags) |
| [Get Taxonomy](actions/get-taxonomy.md) | `GET /wp/v2/taxonomies/{taxonomy}` | [docs](https://longreads.com/wp-json/wp/v2/taxonomies) |
| [Get Taxonomy Index](actions/get-taxonomy-index.md) | `GET /wp/v2/taxonomies` | [docs](https://longreads.com/wp-json/wp/v2/taxonomies) |
| [Get Web App Manifest](actions/get-web-app-manifest.md) | `GET /wp/v2/web-app-manifest` | [docs](https://longreads.com/wp-json/wp/v2/web-app-manifest) |
| [Get Yoast Head Metadata](actions/get-yoast-head-metadata.md) | `GET /yoast/v1/get_head` | [docs](https://longreads.com/wp-json/yoast/v1/get_head) |
| [List Categories](actions/list-categories.md) | `GET /wp/v2/categories` | [docs](https://longreads.com/wp-json/wp/v2/categories) |
| [List Categories By Slug](actions/list-categories-by-slug.md) | `GET /wp/v2/categories` | [docs](https://longreads.com/wp-json/wp/v2/categories) |
| [List Coauthors For Post](actions/list-coauthors-for-post.md) | `GET /coauthors/v1/coauthors` | [docs](https://longreads.com/wp-json/coauthors/v1/coauthors) |
| [List Comments](actions/list-comments.md) | `GET /wp/v2/comments` | [docs](https://longreads.com/wp-json/wp/v2/comments) |
| [List Comments For Post](actions/list-comments-for-post.md) | `GET /wp/v2/comments` | [docs](https://longreads.com/wp-json/wp/v2/comments) |
| [List Guest Authors](actions/list-guest-authors.md) | `GET /wp/v2/guest-author` | [docs](https://longreads.com/wp-json/wp/v2/guest-author) |
| [List Media](actions/list-media.md) | `GET /wp/v2/media` | [docs](https://longreads.com/wp-json/wp/v2/media) |
| [List Pages](actions/list-pages.md) | `GET /wp/v2/pages` | [docs](https://longreads.com/wp-json/wp/v2/pages) |
| [List Pages By Slug](actions/list-pages-by-slug.md) | `GET /wp/v2/pages` | [docs](https://longreads.com/wp-json/wp/v2/pages) |
| [List Posts](actions/list-posts.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [List Posts By Category](actions/list-posts-by-category.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [List Posts By Slug](actions/list-posts-by-slug.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [List Posts By Tag](actions/list-posts-by-tag.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [List Posts Published After Date](actions/list-posts-published-after-date.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [List Posts Published Before Date](actions/list-posts-published-before-date.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [List Tags](actions/list-tags.md) | `GET /wp/v2/tags` | [docs](https://longreads.com/wp-json/wp/v2/tags) |
| [List Tags By Slug](actions/list-tags-by-slug.md) | `GET /wp/v2/tags` | [docs](https://longreads.com/wp-json/wp/v2/tags) |
| [Search Categories](actions/search-categories.md) | `GET /wp/v2/categories` | [docs](https://longreads.com/wp-json/wp/v2/categories) |
| [Search Comments](actions/search-comments.md) | `GET /wp/v2/comments` | [docs](https://longreads.com/wp-json/wp/v2/comments) |
| [Search Guest Authors](actions/search-guest-authors.md) | `GET /wp/v2/guest-author` | [docs](https://longreads.com/wp-json/wp/v2/guest-author) |
| [Search Media](actions/search-media.md) | `GET /wp/v2/media` | [docs](https://longreads.com/wp-json/wp/v2/media) |
| [Search Pages](actions/search-pages.md) | `GET /wp/v2/pages` | [docs](https://longreads.com/wp-json/wp/v2/pages) |
| [Search Posts](actions/search-posts.md) | `GET /wp/v2/posts` | [docs](https://longreads.com/wp-json/wp/v2/posts) |
| [Search Site Content](actions/search-site-content.md) | `GET /wp/v2/search` | [docs](https://longreads.com/wp-json/wp/v2/search) |
| [Search Tags](actions/search-tags.md) | `GET /wp/v2/tags` | [docs](https://longreads.com/wp-json/wp/v2/tags) |
