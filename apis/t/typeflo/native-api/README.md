# Typeflo: Native API Reference

A consolidated summary of Typeflo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://typeflo.io/knowledge-base/category/headless-cms
- **API base URL:** `https://{subdomain}.typeflo.io/api/headless`

## Authentication

### Typeflo API Keys

Use a Typeflo subdomain with separate Content API and Admin API keys.

### Credentials

- **Workspace Subdomain:** `subdomain` · required · Enter only the Typeflo workspace subdomain. For https://acme.typeflo.io, enter acme. Do not include https:// or .typeflo.io.
- **Content API Key:** `contentApiKey` · required · Bearer key for Typeflo content read endpoints.
- **Admin API Key:** `adminApiKey` · required · Bearer key for Typeflo admin write endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <contentApiKey>
Authorization: Bearer <adminApiKey>
```

[Official authentication documentation](https://typeflo.io/knowledge-base/category/headless-cms)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size. Use `start_range` in the query string to choose the result range; numbering starts at 0.

## Filtering

Send filters in the query string.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | `POST /admin/category` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Create Post](actions/create-post.md) | `POST /admin/posts` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Create Tag](actions/create-tag.md) | `POST /admin/tags` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Delete Category](actions/delete-category.md) | `DELETE /admin/category/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Delete Post](actions/delete-post.md) | `DELETE /admin/posts/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /admin/tags/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Get Author](actions/get-author.md) | `GET /content/authors/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Author By Slug](actions/get-author-by-slug.md) | `GET /content/authors/:slug` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Category](actions/get-category.md) | `GET /content/category/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Category By Slug](actions/get-category-by-slug.md) | `GET /content/category/:slug` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Page](actions/get-page.md) | `GET /content/pages/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Page By Slug](actions/get-page-by-slug.md) | `GET /content/pages/:slug` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Post](actions/get-post.md) | `GET /content/posts/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Post By Slug](actions/get-post-by-slug.md) | `GET /content/posts/:slug` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Tag](actions/get-tag.md) | `GET /content/tags/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Get Tag By Slug](actions/get-tag-by-slug.md) | `GET /content/tags/:slug` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [List Authors](actions/list-authors.md) | `GET /content/authors` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [List Categories](actions/list-categories.md) | `GET /content/category` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [List Pages](actions/list-pages.md) | `GET /content/pages` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [List Posts](actions/list-posts.md) | `GET /content/posts` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [List Tags](actions/list-tags.md) | `GET /content/tags` | [docs](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation) |
| [Update Category](actions/update-category.md) | `PATCH /admin/category/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Update Post](actions/update-post.md) | `PATCH /admin/posts/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
| [Update Tag](actions/update-tag.md) | `PATCH /admin/tags/:id` | [docs](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation) |
