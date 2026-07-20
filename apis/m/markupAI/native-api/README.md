# Markup AI: Native API Reference

A consolidated summary of Markup AI's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.markup.ai/
- **OpenAPI specification:** https://docs.markup.ai/openapi.json
- **API base URL:** `https://api.markup.ai`

## Authentication

### API Key

Authenticate Markup AI requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.markup.ai/quickstart)

## API conventions

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `page`.

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | `POST /v1/terminology/domains` | [docs](https://docs.markup.ai/api-reference/terminology/create-domain) |
| [Create Style Check](actions/create-style-check.md) | `POST /v1/style/checks` | [docs](https://docs.markup.ai/api-reference/style-checks/create-style-check) |
| [Create Style Guide](actions/create-style-guide.md) | `POST /v1/style-guides` | [docs](https://docs.markup.ai/api-reference/style-guides/create-style-guide) |
| [Create Style Rewrite](actions/create-style-rewrite.md) | `POST /v1/style/rewrites` | [docs](https://docs.markup.ai/api-reference/style-rewrites/create-style-rewrite) |
| [Create Style Suggestion](actions/create-style-suggestion.md) | `POST /v1/style/suggestions` | [docs](https://docs.markup.ai/api-reference/style-suggestions/create-style-suggestion) |
| [Create Term](actions/create-term.md) | `POST /v1/terminology/term-sets/:term_set_id/terms` | [docs](https://docs.markup.ai/api-reference/terminology/create-term) |
| [Create Term Set](actions/create-term-set.md) | `POST /v1/terminology/term-sets` | [docs](https://docs.markup.ai/api-reference/terminology/create-term-set) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /v1/terminology/domains/:domain_id` | [docs](https://docs.markup.ai/api-reference/terminology/delete-domain) |
| [Delete Style Guide](actions/delete-style-guide.md) | `DELETE /v1/style-guides/:style_guide_id` | [docs](https://docs.markup.ai/api-reference/style-guides/delete-style-guide) |
| [Delete Term](actions/delete-term.md) | `DELETE /v1/terminology/term-sets/:term_set_id/terms/:term_id` | [docs](https://docs.markup.ai/api-reference/terminology/delete-term) |
| [Delete Term Set](actions/delete-term-set.md) | `DELETE /v1/terminology/term-sets/:term_set_id` | [docs](https://docs.markup.ai/api-reference/terminology/delete-term-set) |
| [Get Domain](actions/get-domain.md) | `GET /v1/terminology/domains/:domain_id` | [docs](https://docs.markup.ai/api-reference/terminology/get-domain) |
| [Get Style Check](actions/get-style-check.md) | `GET /v1/style/checks/:workflow_id` | [docs](https://docs.markup.ai/api-reference/style-checks/get-style-check) |
| [Get Style Guide](actions/get-style-guide.md) | `GET /v1/style-guides/:style_guide_id` | [docs](https://docs.markup.ai/api-reference/style-guides/get-style-guide) |
| [Get Style Rewrite](actions/get-style-rewrite.md) | `GET /v1/style/rewrites/:workflow_id` | [docs](https://docs.markup.ai/api-reference/style-rewrites/get-style-rewrite) |
| [Get Style Suggestion](actions/get-style-suggestion.md) | `GET /v1/style/suggestions/:workflow_id` | [docs](https://docs.markup.ai/api-reference/style-suggestions/get-style-suggestion) |
| [Get Term](actions/get-term.md) | `GET /v1/terminology/term-sets/:term_set_id/terms/:term_id` | [docs](https://docs.markup.ai/api-reference/terminology/get-term) |
| [Get Term Set](actions/get-term-set.md) | `GET /v1/terminology/term-sets/:term_set_id` | [docs](https://docs.markup.ai/api-reference/terminology/get-term-set) |
| [List Domains](actions/list-domains.md) | `GET /v1/terminology/domains` | [docs](https://docs.markup.ai/api-reference/terminology/list-domains) |
| [List Style Guides](actions/list-style-guides.md) | `GET /v1/style-guides` | [docs](https://docs.markup.ai/api-reference/style-guides/list-style-guides) |
| [List Term Sets](actions/list-term-sets.md) | `GET /v1/terminology/term-sets` | [docs](https://docs.markup.ai/api-reference/terminology/list-term-sets) |
| [Search Terminology](actions/search-terminology.md) | `GET /v1/terminology/search` | [docs](https://docs.markup.ai/api-reference/terminology/search-terminology) |
| [Update Domain](actions/update-domain.md) | `PATCH /v1/terminology/domains/:domain_id` | [docs](https://docs.markup.ai/api-reference/terminology/update-domain) |
| [Update Style Guide](actions/update-style-guide.md) | `PATCH /v1/style-guides/:style_guide_id` | [docs](https://docs.markup.ai/api-reference/style-guides/update-style-guide) |
| [Update Term](actions/update-term.md) | `PUT /v1/terminology/term-sets/:term_set_id/terms/:term_id` | [docs](https://docs.markup.ai/api-reference/terminology/update-term) |
| [Update Term Set](actions/update-term-set.md) | `PATCH /v1/terminology/term-sets/:term_set_id` | [docs](https://docs.markup.ai/api-reference/terminology/update-term-set) |
