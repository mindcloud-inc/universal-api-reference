# SE Ranking Data: Native API Reference

A consolidated summary of SE Ranking Data's API configuration and 60 documented operations, with links to official documentation.

- **Official docs:** https://seranking.com/api.html
- **API base URL:** `https://api.seranking.com/v1`

## Authentication

### API Token

SE Ranking Data API token. Supported by Authorization: Token <API_TOKEN> header or apikey query parameter per official docs.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://seranking.com/api/data/getting-started/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_field` in the query string. Set the direction separately with `order_type`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (60 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze keyword overlap and gaps](actions/analyze-keyword-overlap-and-gaps.md) | `GET /domain/keywords/comparison` | [docs](https://seranking.com/api/data/domain-analysis/#domain-comparison) |
| [Create advanced audit](actions/create-advanced-audit.md) | `POST /site-audit/audits/advanced` | [docs](https://seranking.com/api/data/website-audit/#create-audit-advanced) |
| [Create standard audit](actions/create-standard-audit.md) | `POST /site-audit/audits/standard` | [docs](https://seranking.com/api/data/website-audit/#create-audit-standard) |
| [Delete audit](actions/delete-audit.md) | `DELETE /site-audit/audits` | [docs](https://seranking.com/api/data/website-audit/#delete-audit) |
| [Discover brand by URL](actions/discover-brand-by-url.md) | `GET /ai-search/discover-brand` | [docs](https://seranking.com/api/data/ai-search/#discover-brand-by-url) |
| [Export backlinks data](actions/export-backlinks-data.md) | `GET /backlinks/export` | [docs](https://seranking.com/api/data/backlinks/#export) |
| [Export keyword metrics](actions/export-keyword-metrics.md) | `POST /keywords/export` | [docs](https://seranking.com/api/data/keyword-research/#export) |
| [Fetch backlinks in batches](actions/fetch-backlinks-in-batches.md) | `GET /backlinks/raw` | [docs](https://seranking.com/api/data/backlinks/#raw) |
| [Get AI search leaderboard](actions/get-ai-search-leaderboard.md) | `POST /ai-search/overview/leaderboard` | [docs](https://seranking.com/api/data/ai-search/) |
| [Get AI search overview](actions/get-ai-search-overview.md) | `GET /ai-search/overview/by-engine/time-series` | [docs](https://seranking.com/api/data/ai-search/#overview) |
| [Get all crawled pages](actions/get-all-crawled-pages.md) | `GET /site-audit/audits/pages` | [docs](https://seranking.com/api/data/website-audit/#get-all-crawled-pages) |
| [Get all found links](actions/get-all-found-links.md) | `GET /site-audit/audits/links` | [docs](https://seranking.com/api/data/website-audit/#get-all-found-links) |
| [Get all issues by URL](actions/get-all-issues-by-url.md) | `GET /site-audit/audits/issues` | [docs](https://seranking.com/api/data/website-audit/#get-all-issues-for-a-specific-url) |
| [Get audit history by date](actions/get-audit-history-by-date.md) | `GET /site-audit/audits/history` | [docs](https://seranking.com/api/data/website-audit/#get-audit-history-by-date) |
| [Get audit pages by issue](actions/get-audit-pages-by-issue.md) | `GET /site-audit/audits/issue-pages` | [docs](https://seranking.com/api/data/website-audit/#get-audit-pages-by-issue) |
| [Get audit report](actions/get-audit-report.md) | `GET /site-audit/audits/report` | [docs](https://seranking.com/api/data/website-audit/#get-audit-report) |
| [Get audit status](actions/get-audit-status.md) | `GET /site-audit/audits/status` | [docs](https://seranking.com/api/data/website-audit/#get-audit-status) |
| [Get backlink anchor texts](actions/get-backlink-anchor-texts.md) | `GET /backlinks/anchors` | [docs](https://seranking.com/api/data/backlinks/#anchors) |
| [Get backlink metrics](actions/get-backlink-metrics.md) | `GET /backlinks/metrics` | [docs](https://seranking.com/api/data/backlinks/#metrics) |
| [Get backlink summary](actions/get-backlink-summary.md) | `GET /backlinks/summary` | [docs](https://seranking.com/api/data/backlinks/#summary) |
| [Get cumulative backlinks over time](actions/get-cumulative-backlinks-over-time.md) | `GET /backlinks/history/cumulative` | [docs](https://seranking.com/api/data/backlinks/#history-cumulative) |
| [Get daily count of new and lost backlinks](actions/get-daily-count-of-new-and-lost-backlinks.md) | `GET /backlinks/history/count` | [docs](https://seranking.com/api/data/backlinks/#history-count) |
| [Get daily count of new and lost referring domains](actions/get-daily-count-of-new-and-lost-referring-domains.md) | `GET /backlinks/refdomains/history/count` | [docs](https://seranking.com/api/data/backlinks/#refdomains-history-count) |
| [Get domain authority](actions/get-domain-authority.md) | `GET /backlinks/authority/domain` | [docs](https://seranking.com/api/data/backlinks/#authority-domain) |
| [Get domain authority distribution](actions/get-domain-authority-distribution.md) | `GET /backlinks/authority/domain/distribution` | [docs](https://seranking.com/api/data/backlinks/#authority-domain-distribution) |
| [Get domain authority history](actions/get-domain-authority-history.md) | `GET /backlinks/authority/domain/history` | [docs](https://seranking.com/api/data/backlinks/#authority-domain-history) |
| [Get domain competitors](actions/get-domain-competitors.md) | `GET /domain/competitors` | [docs](https://seranking.com/api/data/domain-analysis/#competitors) |
| [Get Domain Keyword Rankings](actions/get-domain-keyword-rankings.md) | `GET /domain/keywords` | [docs](https://seranking.com/api/data/domain-analysis/#domain-keywords) |
| [Get Domain Overview by Region](actions/get-domain-overview-by-region.md) | `GET /domain/overview/db` | [docs](https://seranking.com/api/data/domain-analysis/#regional-database) |
| [Get domain pages](actions/get-domain-pages.md) | `GET /domain/pages` | [docs](https://seranking.com/api/data/domain-analysis/#domain-pages) |
| [Get domain subdomains](actions/get-domain-subdomains.md) | `GET /domain/subdomains` | [docs](https://seranking.com/api/data/domain-analysis/#domain-subdomains) |
| [Get domain traffic and keyword history](actions/get-domain-traffic-and-keyword-history.md) | `GET /domain/overview/history` | [docs](https://seranking.com/api/data/domain-analysis/#history-trends) |
| [Get longtail keywords](actions/get-longtail-keywords.md) | `GET /keywords/longtail` | [docs](https://seranking.com/api/data/keyword-research/#longtail) |
| [Get page and domain authority](actions/get-page-and-domain-authority.md) | `GET /backlinks/authority` | [docs](https://seranking.com/api/data/backlinks/#authority) |
| [Get page authority](actions/get-page-authority.md) | `GET /backlinks/authority/page` | [docs](https://seranking.com/api/data/backlinks/#authority-page) |
| [Get page authority history](actions/get-page-authority-history.md) | `GET /backlinks/authority/page/history` | [docs](https://seranking.com/api/data/backlinks/#authority-page-history) |
| [Get paid ads by keyword](actions/get-paid-ads-by-keyword.md) | `GET /domain/ads` | [docs](https://seranking.com/api/data/domain-analysis/#paid-ads-keyword) |
| [Get paid ads for domain](actions/get-paid-ads-for-domain.md) | `GET /domain/ads` | [docs](https://seranking.com/api/data/domain-analysis/#paid-ads-domain) |
| [Get prompts by brand](actions/get-prompts-by-brand.md) | `GET /ai-search/prompts-by-brand` | [docs](https://seranking.com/api/data/ai-search/#get-prompts-by-brand) |
| [Get prompts by target](actions/get-prompts-by-target.md) | `GET /ai-search/prompts-by-target` | [docs](https://seranking.com/api/data/ai-search/#get-prompts-by-target) |
| [Get question keywords](actions/get-question-keywords.md) | `GET /keywords/questions` | [docs](https://seranking.com/api/data/keyword-research/#questions) |
| [Get related keywords](actions/get-related-keywords.md) | `GET /keywords/related` | [docs](https://seranking.com/api/data/keyword-research/#related) |
| [Get similar keywords](actions/get-similar-keywords.md) | `GET /keywords/similar` | [docs](https://seranking.com/api/data/keyword-research/#similar) |
| [Get Subscription Details](actions/get-subscription-details.md) | `GET /account/subscription` | [docs](https://seranking.com/api/data/get-data/account/subscription.html) |
| [Get total backlinks count](actions/get-total-backlinks-count.md) | `GET /backlinks/count` | [docs](https://seranking.com/api/data/backlinks/#count) |
| [Get total referring domains count](actions/get-total-referring-domains-count.md) | `GET /backlinks/refdomains/count` | [docs](https://seranking.com/api/data/backlinks/#refdomains-count) |
| [Get total referring IPs count](actions/get-total-referring-ips-count.md) | `GET /backlinks/referring-ips/count` | [docs](https://seranking.com/api/data/backlinks/#referring-ips-count) |
| [Get total referring subnets count](actions/get-total-referring-subnets-count.md) | `GET /backlinks/referring-subnets/count` | [docs](https://seranking.com/api/data/backlinks/#referring-subnets-count) |
| [Get Worldwide Domain Overview](actions/get-worldwide-domain-overview.md) | `GET /domain/overview/worldwide` | [docs](https://seranking.com/api/data/domain-analysis/#worldwide-aggregate) |
| [Get worldwide URL overview](actions/get-worldwide-url-overview.md) | `GET /domain/overview/worldwide/url` | [docs](https://seranking.com/api/data/domain-analysis/#worldwide-aggregate-url) |
| [List all backlinks](actions/list-all-backlinks.md) | `GET /backlinks/all` | [docs](https://seranking.com/api/data/backlinks/#all) |
| [List audits](actions/list-audits.md) | `GET /site-audit/audits` | [docs](https://seranking.com/api/data/website-audit/#list-audits) |
| [List indexed pages with backlinks](actions/list-indexed-pages-with-backlinks.md) | `GET /backlinks/indexed-pages` | [docs](https://seranking.com/api/data/backlinks/#indexed-pages) |
| [List new and lost backlinks](actions/list-new-and-lost-backlinks.md) | `GET /backlinks/history` | [docs](https://seranking.com/api/data/backlinks/#history) |
| [List new and lost referring domains](actions/list-new-and-lost-referring-domains.md) | `GET /backlinks/refdomains/history` | [docs](https://seranking.com/api/data/backlinks/#refdomains-history) |
| [List referring domains](actions/list-referring-domains.md) | `GET /backlinks/refdomains` | [docs](https://seranking.com/api/data/backlinks/#refdomains) |
| [List referring IPs](actions/list-referring-ips.md) | `GET /backlinks/referring-ips` | [docs](https://seranking.com/api/data/backlinks/#referring-ips) |
| [Recheck advanced audit](actions/recheck-advanced-audit.md) | `POST /site-audit/audits/recheck/advanced` | [docs](https://seranking.com/api/data/website-audit/#recheck-audit-advanced) |
| [Recheck standard audit](actions/recheck-standard-audit.md) | `POST /site-audit/audits/recheck/standard` | [docs](https://seranking.com/api/data/website-audit/#recheck-audit-standard) |
| [Update audit title](actions/update-audit-title.md) | `PATCH /site-audit/audits` | [docs](https://seranking.com/api/data/website-audit/#update-audit-title) |
