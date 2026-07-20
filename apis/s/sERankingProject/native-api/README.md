# SE Ranking Project: Native API Reference

A consolidated summary of SE Ranking Project's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://seranking.com/api/project/
- **API base URL:** `https://api4.seranking.com`

## Authentication

### Project API Key

Authenticate SE Ranking Project API requests with your project-specific API key (40-char hex).

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://seranking.com/api/project/getting-started/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Competitor](actions/add-competitor.md) | `POST /competitors` | [docs](https://seranking.com/api/project/competitors/#add-competitor) |
| [Add Keyword Group](actions/add-keyword-group.md) | `POST /keyword-groups` | [docs](https://seranking.com/api/project/keyword-groups/#add-keyword-group) |
| [Add Keywords to Project](actions/add-keywords-to-project.md) | `POST /sites/:site_id/keywords` | [docs](https://seranking.com/api/project/project-management/#add-queries-to-project) |
| [Add Project](actions/add-project.md) | `POST /sites` | [docs](https://seranking.com/api/project/project-management/#adding-a-project) |
| [Add Search Engine To Project](actions/add-search-engine-to-project.md) | `POST /sites/:site_id/search-engines` | [docs](https://seranking.com/api/project/project-management/#add-search-engine-to-project) |
| [Delete Competitor](actions/delete-competitor.md) | `DELETE /competitors/:competitor_id` | [docs](https://seranking.com/api/project/competitors/#delete-competitor) |
| [Delete Keywords from Project](actions/delete-keywords-from-project.md) | `DELETE /sites/:site_id/keywords` | [docs](https://seranking.com/api/project/project-management/#delete-keywords) |
| [Delete Project](actions/delete-project.md) | `DELETE /sites/:site_id` | [docs](https://seranking.com/api/project/project-management/#delete-project) |
| [Delete Search Engine From Project](actions/delete-search-engine-from-project.md) | `DELETE /sites/:site_id/search-engines/:site_engine_id` | [docs](https://seranking.com/api/project/project-management/#delete-search-engine-from-project) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/balance` | [docs](https://seranking.com/api/project/account/#account-balance) |
| [Get Competitor Keyword Positions](actions/get-competitor-keyword-positions.md) | `GET /competitors/:competitor_id/positions` | [docs](https://seranking.com/api/project/competitors/#get-competitor-keyword-positions) |
| [Get Keyword Statistics](actions/get-keyword-statistics.md) | `GET /sites/:site_id/positions` | [docs](https://seranking.com/api/project/project-management/#keyword-statistics) |
| [Get Project Summary Statistics](actions/get-project-summary-statistics.md) | `GET /sites/:site_id/stat` | [docs](https://seranking.com/api/project/project-management/#summary-statistics) |
| [Get Subscription Data](actions/get-subscription-data.md) | `GET /account/subscription` | [docs](https://seranking.com/api/project/account/#subscription-data) |
| [Get Total Number Of Ads Chart](actions/get-total-number-of-ads-chart.md) | `GET /sites/:site_id/ads` | [docs](https://seranking.com/api/project/project-management/#total-number-of-ads-chart) |
| [Get User Profile](actions/get-user-profile.md) | `GET /account/profile` | [docs](https://seranking.com/api/project/account/#user-profile) |
| [List All Competitors](actions/list-all-competitors.md) | `GET /competitors/all/:site_id` | [docs](https://seranking.com/api/project/competitors/#get-all-competitors) |
| [List Competitors](actions/list-competitors.md) | `GET /competitors/site/:site_id` | [docs](https://seranking.com/api/project/competitors/#list-competitors) |
| [List Historical Dates](actions/list-historical-dates.md) | `GET /sites/:site_id/historicalDates` | [docs](https://seranking.com/api/project/project-management/#historical-dates) |
| [List Keyword Groups](actions/list-keyword-groups.md) | `GET /keyword-groups/:site_id` | [docs](https://seranking.com/api/project/keyword-groups/#list-keyword-groups) |
| [List Project Search Engines](actions/list-project-search-engines.md) | `GET /sites/:site_id/search-engines` | [docs](https://seranking.com/api/project/project-management/#list-project-search-engines) |
| [List Projects](actions/list-projects.md) | `GET /sites` | [docs](https://seranking.com/api/project/project-management/#list-projects) |
| [List Top 10 Results](actions/list-top10-results.md) | `GET /competitors/top10/:site_id` | [docs](https://seranking.com/api/project/competitors/#get-top-10-results) |
| [List Top 100 Results](actions/list-top100-results.md) | `GET /competitors/top100/:site_id` | [docs](https://seranking.com/api/project/competitors/#get-top-100-results) |
| [List Website Keywords](actions/list-website-keywords.md) | `GET /sites/:site_id/keywords` | [docs](https://seranking.com/api/project/project-management/#website-keyword-list) |
| [Rename Keyword Group](actions/rename-keyword-group.md) | `PUT /keyword-groups/:group_id` | [docs](https://seranking.com/api/project/keyword-groups/#rename-keyword-group) |
| [Run Position Check](actions/run-position-check.md) | `POST /api/sites/:site_id/recheck` | [docs](https://seranking.com/api/project/project-management/#run-position-check) |
| [Set Manual Position](actions/set-manual-position.md) | `PUT /sites/:site_id/position` | [docs](https://seranking.com/api/project/project-management/#set-manual-position) |
| [Update Project Settings](actions/update-project-settings.md) | `PUT /sites/:site_id` | [docs](https://seranking.com/api/project/project-management/#change-project-settings) |
| [Update Search Engine in Project](actions/update-search-engine-in-project.md) | `PUT /sites/:site_id/search-engines/:site_engine_id` | [docs](https://seranking.com/api/project/project-management/#change-search-engine-in-project) |
