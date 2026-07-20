# SEOTakeoff: Native API Reference

A consolidated summary of SEOTakeoff's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.seotakeoff.com/docs
- **OpenAPI specification:** https://api.seotakeoff.com/openapi.json
- **API base URL:** `https://api.seotakeoff.com`

## Authentication

### API Key

Authenticate with your SEOTakeoff API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.seotakeoff.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; maximum 100).

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Suggestions](actions/autocomplete-suggestions.md) | `GET /api/v1/tools/autocomplete` | [docs](https://api.seotakeoff.com/docs) |
| [Check Links](actions/check-links.md) | `POST /api/v1/tools/check-links` | [docs](https://api.seotakeoff.com/docs) |
| [Create Generation Job](actions/create-generation-job.md) | `POST /api/v1/generate` | [docs](https://api.seotakeoff.com/docs) |
| [Get Backlink Network Stats](actions/get-backlink-network-stats.md) | `GET /api/v1/backlink-network/stats` | [docs](https://api.seotakeoff.com/docs) |
| [List Articles](actions/list-articles.md) | `GET /api/zapier/articles` | [docs](https://api.seotakeoff.com/docs) |
| [List Clusters](actions/list-clusters.md) | `GET /api/zapier/clusters` | [docs](https://api.seotakeoff.com/docs) |
| [List Clusters Dropdown](actions/list-clusters-dropdown.md) | `GET /api/zapier/clusters/dropdown` | [docs](https://api.seotakeoff.com/docs) |
| [List Jobs](actions/list-jobs.md) | `GET /api/v1/jobs` | [docs](https://api.seotakeoff.com/docs) |
| [List Keywords](actions/list-keywords.md) | `GET /api/zapier/keywords` | [docs](https://api.seotakeoff.com/docs) |
| [List Plans](actions/list-plans.md) | `GET /api/v1/stripe/plans` | [docs](https://api.seotakeoff.com/docs) |
| [List Websites](actions/list-websites.md) | `GET /api/zapier/websites` | [docs](https://api.seotakeoff.com/docs) |
| [Queue Article](actions/queue-article.md) | `POST /api/zapier/articles/queue` | [docs](https://api.seotakeoff.com/docs) |
| [Research Keywords](actions/research-keywords.md) | `POST /api/zapier/clusters/research-keywords` | [docs](https://api.seotakeoff.com/docs) |
| [Schedule Article](actions/schedule-article.md) | `POST /api/zapier/articles/schedule` | [docs](https://api.seotakeoff.com/docs) |
| [Schedule Queued Article](actions/schedule-queued-article.md) | `POST /api/v1/article-queue/schedule` | [docs](https://api.seotakeoff.com/docs) |
| [Score Article Quality](actions/score-article-quality.md) | `POST /api/v1/quality/score` | [docs](https://api.seotakeoff.com/docs) |
| [Search Articles](actions/search-articles.md) | `GET /api/zapier/articles/search` | [docs](https://api.seotakeoff.com/docs) |
| [Search Clusters](actions/search-clusters.md) | `GET /api/zapier/clusters/search` | [docs](https://api.seotakeoff.com/docs) |
| [Search Websites](actions/search-websites.md) | `GET /api/zapier/websites/search` | [docs](https://api.seotakeoff.com/docs) |
| [Trigger Ranking Snapshot](actions/trigger-ranking-snapshot.md) | `POST /api/v1/rankings/snapshot` | [docs](https://api.seotakeoff.com/docs) |
