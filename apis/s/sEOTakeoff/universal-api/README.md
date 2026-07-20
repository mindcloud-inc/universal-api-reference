# <img src="https://images.mindcloud.co/apps/icons/s-eotakeoff_1777305254504.png" alt="SEOTakeoff logo" width="28" height="28"> SEOTakeoff: Universal API

Find keywords, generate SEO articles, and publish content to your CMS

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sEOTakeoff/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.seotakeoff.com
- **Vendor API docs:** https://api.seotakeoff.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Jobs](actions/list-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-jobs?connectionId=$CONNECTION_ID&tenantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Articles](actions/list-articles.md) | GET |  |
| [Queue Article](actions/queue-article.md) | POST |  |
| [Search Articles](actions/search-articles.md) | GET |  |

### Article Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Schedule Article](actions/schedule-article.md) | PUT |  |

### Autocomplete Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Suggestions](actions/autocomplete-suggestions.md) | GET |  |

### Backlink Network Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Backlink Network Stats](actions/get-backlink-network-stats.md) | GET |  |

### Cluster

| Action | Method | Description |
| --- | --- | --- |
| [List Clusters](actions/list-clusters.md) | GET |  |
| [List Clusters Dropdown](actions/list-clusters-dropdown.md) | GET |  |
| [Search Clusters](actions/search-clusters.md) | GET |  |

### Cluster Research

| Action | Method | Description |
| --- | --- | --- |
| [Research Keywords](actions/research-keywords.md) | POST |  |

### Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Generation Job](actions/create-generation-job.md) | POST |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET |  |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [List Keywords](actions/list-keywords.md) | GET |  |

### Link Check Result

| Action | Method | Description |
| --- | --- | --- |
| [Check Links](actions/check-links.md) | GET |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET |  |

### Quality Score

| Action | Method | Description |
| --- | --- | --- |
| [Score Article Quality](actions/score-article-quality.md) | GET |  |

### Queued Article Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Schedule Queued Article](actions/schedule-queued-article.md) | PUT |  |

### Ranking Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Ranking Snapshot](actions/trigger-ranking-snapshot.md) | POST |  |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [List Websites](actions/list-websites.md) | GET |  |
| [Search Websites](actions/search-websites.md) | GET |  |

