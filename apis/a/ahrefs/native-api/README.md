# Ahrefs: Native API Reference

A consolidated summary of Ahrefs's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.ahrefs.com/en/api/docs/introduction
- **API base URL:** `https://api.ahrefs.com/v3`

## Authentication

### API Key

Authenticate requests to Ahrefs API v3 with an API key sent as a bearer token.

### Credentials

- **Ahrefs API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ahrefs.com/en/api/docs/api-keys-creation-and-management)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000).

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Backlinks Stats](actions/get-backlinks-stats.md) | `GET /site-explorer/backlinks-stats` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-backlinks-stats) |
| [Get Domain Rating](actions/get-domain-rating.md) | `GET /site-explorer/domain-rating` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-domain-rating) |
| [Get Keyword Volume History](actions/get-keyword-volume-history.md) | `GET /keywords-explorer/volume-history` | [docs](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-volume-history) |
| [Get Keywords Overview](actions/get-keywords-overview.md) | `GET /keywords-explorer/overview` | [docs](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-overview) |
| [Get Limits And Usage](actions/get-limits-and-usage.md) | `GET /subscription-info/limits-and-usage` | [docs](https://docs.ahrefs.com/en/api/reference/subscription-info/get-limits-and-usage) |
| [Get Metrics History](actions/get-metrics-history.md) | `GET /site-explorer/metrics-history` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-metrics-history) |
| [Get Public Domain Rating](actions/get-public-domain-rating.md) | `GET /public/domain-rating-free` | [docs](https://docs.ahrefs.com/en/api/reference/public/get-domain-rating-free) |
| [Get Refdomains History](actions/get-refdomains-history.md) | `GET /site-explorer/refdomains-history` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-refdomains-history) |
| [Get SERP Overview](actions/get-serp-overview.md) | `GET /serp-overview/serp-overview` | [docs](https://docs.ahrefs.com/en/api/reference/serp-overview/get-serp-overview) |
| [Get Site Metrics](actions/get-site-metrics.md) | `GET /site-explorer/metrics` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-metrics) |
| [List Anchors](actions/list-anchors.md) | `GET /site-explorer/anchors` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-anchors) |
| [List Backlinks](actions/list-backlinks.md) | `GET /site-explorer/all-backlinks` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-all-backlinks) |
| [List Linked Domains](actions/list-linked-domains.md) | `GET /site-explorer/linkeddomains` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-linkeddomains) |
| [List Matching Terms](actions/list-matching-terms.md) | `GET /keywords-explorer/matching-terms` | [docs](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-matching-terms) |
| [List Metrics By Country](actions/list-metrics-by-country.md) | `GET /site-explorer/metrics-by-country` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-metrics-by-country) |
| [List Organic Competitors](actions/list-organic-competitors.md) | `GET /site-explorer/organic-competitors` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-organic-competitors) |
| [List Organic Keywords](actions/list-organic-keywords.md) | `GET /site-explorer/organic-keywords` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-organic-keywords) |
| [List Pages By Backlinks](actions/list-pages-by-backlinks.md) | `GET /site-explorer/pages-by-backlinks` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-pages-by-backlinks) |
| [List Paid Pages](actions/list-paid-pages.md) | `GET /site-explorer/paid-pages` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-paid-pages) |
| [List Referring Domains](actions/list-referring-domains.md) | `GET /site-explorer/refdomains` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-refdomains) |
| [List Related Terms](actions/list-related-terms.md) | `GET /keywords-explorer/related-terms` | [docs](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-related-terms) |
| [List Search Suggestions](actions/list-search-suggestions.md) | `GET /keywords-explorer/search-suggestions` | [docs](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-search-suggestions) |
| [List Top Pages](actions/list-top-pages.md) | `GET /site-explorer/top-pages` | [docs](https://docs.ahrefs.com/en/api/reference/site-explorer/get-top-pages) |
| [Run Batch Analysis](actions/run-batch-analysis.md) | `POST /batch-analysis/batch-analysis` | [docs](https://docs.ahrefs.com/en/api/reference/batch-analysis/post-batch-analysis) |
