# <img src="https://images.mindcloud.co/apps/icons/vector_1783535057491.png" alt="Ahrefs logo" width="28" height="28"> Ahrefs: Universal API

Access Ahrefs API v3 SEO, backlink, keyword, SERP, batch analysis, and subscription data from an Ahrefs workspace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ahrefs/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ahrefs.com
- **Vendor API docs:** https://docs.ahrefs.com/en/api/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Limits And Usage](actions/get-limits-and-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-limits-and-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Volume History](actions/get-keyword-volume-history.md) | GET |  |
| [Get Keywords Overview](actions/get-keywords-overview.md) | GET |  |
| [List Matching Terms](actions/list-matching-terms.md) | GET |  |
| [List Organic Keywords](actions/list-organic-keywords.md) | GET |  |
| [List Related Terms](actions/list-related-terms.md) | GET |  |
| [List Search Suggestions](actions/list-search-suggestions.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Backlinks Stats](actions/get-backlinks-stats.md) | GET |  |
| [Get Domain Rating](actions/get-domain-rating.md) | GET |  |
| [Get Metrics History](actions/get-metrics-history.md) | GET |  |
| [Get Public Domain Rating](actions/get-public-domain-rating.md) | GET |  |
| [Get Refdomains History](actions/get-refdomains-history.md) | GET |  |
| [Get SERP Overview](actions/get-serp-overview.md) | GET |  |
| [Get Site Metrics](actions/get-site-metrics.md) | GET |  |
| [List Anchors](actions/list-anchors.md) | GET |  |
| [List Backlinks](actions/list-backlinks.md) | GET |  |
| [List Linked Domains](actions/list-linked-domains.md) | GET |  |
| [List Metrics By Country](actions/list-metrics-by-country.md) | GET |  |
| [List Organic Competitors](actions/list-organic-competitors.md) | GET |  |
| [List Pages By Backlinks](actions/list-pages-by-backlinks.md) | GET |  |
| [List Paid Pages](actions/list-paid-pages.md) | GET |  |
| [List Referring Domains](actions/list-referring-domains.md) | GET |  |
| [List Top Pages](actions/list-top-pages.md) | GET |  |
| [Run Batch Analysis](actions/run-batch-analysis.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Limits And Usage](actions/get-limits-and-usage.md) | GET |  |

