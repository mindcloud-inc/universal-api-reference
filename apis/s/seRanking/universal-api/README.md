# <img src="https://images.mindcloud.co/apps/icons/se-ranking_1772139302613.png" alt="SE Ranking Data logo" width="28" height="28"> SE Ranking Data: Universal API

Analyze keywords, backlinks, audits, and SEO data at scale.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seRanking/latest
- **Category:** Marketing
- **Actions:** 60
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seranking.com
- **Vendor API docs:** https://seranking.com/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Subscription Details](actions/get-subscription-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-subscription-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (60)

### Ai Search

| Action | Method | Description |
| --- | --- | --- |
| [Discover brand by URL](actions/discover-brand-by-url.md) | GET | Discovers a brand by URL in SE Ranking Data. |
| [Get AI search leaderboard](actions/get-ai-search-leaderboard.md) | GET | Retrieves the AI search leaderboard from SE Ranking Data. |
| [Get AI search overview](actions/get-ai-search-overview.md) | GET | Retrieves AI search overview data from SE Ranking Data. |
| [Get prompts by brand](actions/get-prompts-by-brand.md) | GET | Retrieves prompts by brand from SE Ranking Data. |
| [Get prompts by target](actions/get-prompts-by-target.md) | GET | Retrieves prompts by target from SE Ranking Data. |

### Backlink

| Action | Method | Description |
| --- | --- | --- |
| [Export backlinks data](actions/export-backlinks-data.md) | GET | Exports backlink data from SE Ranking Data. |
| [Fetch backlinks in batches](actions/fetch-backlinks-in-batches.md) | GET | Retrieves backlinks in batches from SE Ranking Data. |
| [Get backlink anchor texts](actions/get-backlink-anchor-texts.md) | GET | Retrieves backlink anchor texts from SE Ranking Data. |
| [Get backlink metrics](actions/get-backlink-metrics.md) | GET | Retrieves backlink metrics from SE Ranking Data. |
| [Get backlink summary](actions/get-backlink-summary.md) | GET | Retrieves a backlink summary from SE Ranking Data. |
| [Get cumulative backlinks over time](actions/get-cumulative-backlinks-over-time.md) | GET | Retrieves cumulative backlinks over time from SE Ranking Data. |
| [Get daily count of new and lost backlinks](actions/get-daily-count-of-new-and-lost-backlinks.md) | GET | Retrieves daily new and lost backlink counts from SE Ranking Data. |
| [Get daily count of new and lost referring domains](actions/get-daily-count-of-new-and-lost-referring-domains.md) | GET | Retrieves daily new and lost referring domain counts from SE Ranking Data. |
| [Get domain authority](actions/get-domain-authority.md) | GET | Retrieves domain authority from SE Ranking Data. |
| [Get domain authority distribution](actions/get-domain-authority-distribution.md) | GET | Retrieves domain authority distribution from SE Ranking Data. |
| [Get domain authority history](actions/get-domain-authority-history.md) | GET | Retrieves domain authority history from SE Ranking Data. |
| [Get page and domain authority](actions/get-page-and-domain-authority.md) | GET | Retrieves page and domain authority from SE Ranking Data. |
| [Get page authority](actions/get-page-authority.md) | GET | Retrieves page authority from SE Ranking Data. |
| [Get page authority history](actions/get-page-authority-history.md) | GET | Retrieves page authority history from SE Ranking Data. |
| [Get total backlinks count](actions/get-total-backlinks-count.md) | GET | Retrieves the total backlinks count from SE Ranking Data. |
| [Get total referring domains count](actions/get-total-referring-domains-count.md) | GET | Retrieves the total referring domains count from SE Ranking Data. |
| [Get total referring IPs count](actions/get-total-referring-ips-count.md) | GET | Retrieves the total referring IPs count from SE Ranking Data. |
| [Get total referring subnets count](actions/get-total-referring-subnets-count.md) | GET | Retrieves the total referring subnets count from SE Ranking Data. |
| [List all backlinks](actions/list-all-backlinks.md) | GET | Retrieves all backlinks from SE Ranking Data. |
| [List indexed pages with backlinks](actions/list-indexed-pages-with-backlinks.md) | GET | Retrieves indexed pages with backlinks from SE Ranking Data. |
| [List new and lost backlinks](actions/list-new-and-lost-backlinks.md) | GET | Retrieves new and lost backlinks from SE Ranking Data. |
| [List new and lost referring domains](actions/list-new-and-lost-referring-domains.md) | GET | Retrieves new and lost referring domains from SE Ranking Data. |
| [List referring domains](actions/list-referring-domains.md) | GET | Retrieves referring domains from SE Ranking Data. |
| [List referring IPs](actions/list-referring-ips.md) | GET | Retrieves referring IPs from SE Ranking Data. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Analyze keyword overlap and gaps](actions/analyze-keyword-overlap-and-gaps.md) | GET | Analyzes keyword overlap and gaps in SE Ranking Data. |
| [Get domain competitors](actions/get-domain-competitors.md) | GET | Retrieves domain competitors from SE Ranking Data. |
| [Get domain pages](actions/get-domain-pages.md) | GET | Retrieves domain pages from SE Ranking Data. |
| [Get domain subdomains](actions/get-domain-subdomains.md) | GET | Retrieves domain subdomains from SE Ranking Data. |
| [Get domain traffic and keyword history](actions/get-domain-traffic-and-keyword-history.md) | GET | Retrieves domain traffic and keyword history from SE Ranking Data. |
| [Get paid ads by keyword](actions/get-paid-ads-by-keyword.md) | GET | Retrieves paid ads by keyword from SE Ranking Data. |
| [Get paid ads for domain](actions/get-paid-ads-for-domain.md) | GET | Retrieves paid ads for a domain from SE Ranking Data. |
| [Get worldwide URL overview](actions/get-worldwide-url-overview.md) | GET | Retrieves a worldwide URL overview from SE Ranking Data. |

### Domain Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Keyword Rankings](actions/get-domain-keyword-rankings.md) | GET | Retrieves domain keyword rankings from SE Ranking Data. |

### Domain Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Overview by Region](actions/get-domain-overview-by-region.md) | GET | Retrieves a regional domain overview from SE Ranking Data. |
| [Get Worldwide Domain Overview](actions/get-worldwide-domain-overview.md) | GET | Retrieves a worldwide domain overview from SE Ranking Data. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Export keyword metrics](actions/export-keyword-metrics.md) | GET | Exports keyword metrics from SE Ranking Data. |
| [Get longtail keywords](actions/get-longtail-keywords.md) | GET | Retrieves longtail keywords from SE Ranking Data. |
| [Get question keywords](actions/get-question-keywords.md) | GET | Retrieves question keywords from SE Ranking Data. |
| [Get related keywords](actions/get-related-keywords.md) | GET | Retrieves related keywords from SE Ranking Data. |
| [Get similar keywords](actions/get-similar-keywords.md) | GET | Retrieves similar keywords from SE Ranking Data. |

### Site Audit

| Action | Method | Description |
| --- | --- | --- |
| [Create advanced audit](actions/create-advanced-audit.md) | POST | Creates an advanced website audit in SE Ranking Data. |
| [Create standard audit](actions/create-standard-audit.md) | POST | Creates a standard website audit in SE Ranking Data. |
| [Delete audit](actions/delete-audit.md) | DELETE | Deletes an audit from SE Ranking Data. |
| [Get all crawled pages](actions/get-all-crawled-pages.md) | GET | Retrieves all crawled pages from SE Ranking Data. |
| [Get all found links](actions/get-all-found-links.md) | GET | Retrieves all found links from SE Ranking Data. |
| [Get all issues by URL](actions/get-all-issues-by-url.md) | GET | Retrieves all issues by URL from SE Ranking Data. |
| [Get audit history by date](actions/get-audit-history-by-date.md) | GET | Retrieves audit history by date from SE Ranking Data. |
| [Get audit pages by issue](actions/get-audit-pages-by-issue.md) | GET | Retrieves audit pages by issue from SE Ranking Data. |
| [Get audit report](actions/get-audit-report.md) | GET | Retrieves an audit report from SE Ranking Data. |
| [Get audit status](actions/get-audit-status.md) | GET | Retrieves audit status from SE Ranking Data. |
| [List audits](actions/list-audits.md) | GET | Retrieves a list of audits from SE Ranking Data. |
| [Recheck advanced audit](actions/recheck-advanced-audit.md) | PUT | Rechecks an advanced audit in SE Ranking Data. |
| [Recheck standard audit](actions/recheck-standard-audit.md) | PUT | Rechecks a standard audit in SE Ranking Data. |
| [Update audit title](actions/update-audit-title.md) | PUT | Updates an audit title in SE Ranking Data. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Details](actions/get-subscription-details.md) | GET | Retrieves subscription details from SE Ranking Data. |

