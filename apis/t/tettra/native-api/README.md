# Tettra: Native API Reference

A consolidated summary of Tettra's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://support.tettra.com/api-overview
- **API base URL:** `https://app.tettra.co/api`

## Authentication

### API Key

Connect Tettra with an API key.

### Credentials

- **API Key:** `apiKey` · required
- **Team ID:** `teamId` · required · Numeric Tettra team ID used in every Tettra API path.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.tettra.com/api-overview/how-to-find-your-api-credentials)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | `POST /teams/85329/categories` | [docs](https://support.tettra.com/categories-and-subcategories/api-endpoint-create-category) |
| [Create Page](actions/create-page.md) | `POST /teams/85329/pages` | [docs](https://support.tettra.com/pages-2/api-endpoint-create-page) |
| [Create Question](actions/create-question.md) | `POST /teams/85329/questions` | [docs](https://support.tettra.com/api-overview/api-endpoint-create-a-question) |
| [List Category Items](actions/list-category-items.md) | `GET /teams/85329/categories/:category_id` | [docs](https://support.tettra.com/categories-and-subcategories/api-endpoint-get-all-category-items) |
| [Search Pages](actions/search-pages.md) | `GET /teams/85329/search` | [docs](https://support.tettra.com/api-overview/api-endpoint-search) |
| [Suggest New Page](actions/suggest-new-page.md) | `POST /teams/85329/suggestions` | [docs](https://support.tettra.com/pages-2/api-endpoint-suggest-a-new-page) |
| [Suggest Page Update](actions/suggest-page-update.md) | `POST /teams/85329/suggestions` | [docs](https://support.tettra.com/pages-2/api-endpoint-suggest-page-update) |
| [Update Page](actions/update-page.md) | `PATCH /teams/85329/pages/:page_id` | [docs](https://support.tettra.com/pages-2/api-endpoint-update-page) |
