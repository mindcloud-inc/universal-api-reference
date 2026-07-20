# The Guardian: Native API Reference

A consolidated summary of The Guardian's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://open-platform.theguardian.com/documentation/
- **API base URL:** `https://content.guardianapis.com`

## Authentication

### API Key

Guardian Open Platform uses an API key passed as the api-key query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · Your Guardian Open Platform API key. Stored as the single connection secret and sent as the api-key query parameter.

[Official authentication documentation](https://open-platform.theguardian.com/access/)

## API conventions

The total page count is read from `response.pages`. The current page number is read from `response.currentPage`.

## Pagination

Use `page-size` in the query string to set the page size (default 10; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order-by` in the query string. Only one sort field is accepted.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Content By IDs](actions/get-content-by-ids.md) | `GET /search` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/content_search.md) |
| [Get Editors Picks](actions/get-editors-picks.md) | `GET /{{itemPath}}` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Home Editors Picks](actions/get-home-editors-picks.md) | `GET /` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Home Most Viewed](actions/get-home-most-viewed.md) | `GET /` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Item](actions/get-item.md) | `GET /{{itemPath}}` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Most Viewed](actions/get-most-viewed.md) | `GET /{{itemPath}}` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Next Items](actions/get-next-items.md) | `GET /{{itemPath}}/next` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Related Content](actions/get-related-content.md) | `GET /{{itemPath}}` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [Get Story Package](actions/get-story-package.md) | `GET /{{itemPath}}` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md) |
| [List Editions](actions/list-editions.md) | `GET /editions` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/edition.md) |
| [List Sections](actions/list-sections.md) | `GET /sections` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/section.md) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/tag.md) |
| [Search Content](actions/search-content.md) | `GET /search` | [docs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/content_search.md) |
