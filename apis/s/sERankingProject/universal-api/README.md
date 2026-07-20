# <img src="https://images.mindcloud.co/apps/icons/s-eranking-project_1772222055398.png" alt="SE Ranking Project logo" width="28" height="28"> SE Ranking Project: Universal API

Manage SEO projects, track rankings, run audits, and monitor backlinks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sERankingProject/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seranking.com
- **Vendor API docs:** https://seranking.com/api/project/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves your SE Ranking account balance. |
| [Get Subscription Data](actions/get-subscription-data.md) | GET | Retrieves SE Ranking subscription details and account balance. |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves your SE Ranking user profile. |

### Competitor

| Action | Method | Description |
| --- | --- | --- |
| [Add Competitor](actions/add-competitor.md) | POST | Creates a tracked competitor in SE Ranking. |
| [Delete Competitor](actions/delete-competitor.md) | DELETE | Deletes an existing competitor from SE Ranking. |
| [Get Competitor Keyword Positions](actions/get-competitor-keyword-positions.md) | GET | Retrieves competitor keyword rankings from SE Ranking. |
| [List All Competitors](actions/list-all-competitors.md) | GET | Retrieves top-ranked competitor domains from SE Ranking. |
| [List Competitors](actions/list-competitors.md) | GET | Retrieves project competitors from SE Ranking. |
| [List Top 10 Results](actions/list-top10-results.md) | GET | Retrieves top 10 ranking results from SE Ranking. |
| [List Top 100 Results](actions/list-top100-results.md) | GET | Retrieves top 100 ranking results from SE Ranking. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Add Keyword Group](actions/add-keyword-group.md) | POST | Creates a new keyword group in SE Ranking. |
| [Add Keywords to Project](actions/add-keywords-to-project.md) | POST | Adds keywords to an existing SE Ranking project. |
| [Delete Keywords from Project](actions/delete-keywords-from-project.md) | DELETE | Deletes project keywords from SE Ranking. |
| [Get Keyword Statistics](actions/get-keyword-statistics.md) | GET | Retrieves keyword ranking statistics from SE Ranking. |
| [Get Total Number Of Ads Chart](actions/get-total-number-of-ads-chart.md) | GET | Retrieves keyword ad counts by date from SE Ranking. |
| [List Historical Dates](actions/list-historical-dates.md) | GET | Retrieves historical ranking dates from SE Ranking. |
| [List Keyword Groups](actions/list-keyword-groups.md) | GET | Retrieves keyword groups from SE Ranking. |
| [List Website Keywords](actions/list-website-keywords.md) | GET | Retrieves project keywords and basic statistics from SE Ranking. |
| [Rename Keyword Group](actions/rename-keyword-group.md) | PUT | Updates an existing keyword group in SE Ranking. |
| [Run Position Check](actions/run-position-check.md) | POST | Triggers a keyword position check in SE Ranking. |
| [Set Manual Position](actions/set-manual-position.md) | PUT | Updates a keyword's ranking position in SE Ranking. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project](actions/add-project.md) | POST | Creates a new project in SE Ranking. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from SE Ranking. |
| [Get Project Summary Statistics](actions/get-project-summary-statistics.md) | GET | Retrieves project summary statistics from SE Ranking. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your SE Ranking account. |
| [Update Project Settings](actions/update-project-settings.md) | PUT | Updates an existing project in SE Ranking. |

### Searchengine

| Action | Method | Description |
| --- | --- | --- |
| [Add Search Engine To Project](actions/add-search-engine-to-project.md) | POST | Creates a project search engine in SE Ranking. |
| [Delete Search Engine From Project](actions/delete-search-engine-from-project.md) | DELETE | Deletes a project search engine from SE Ranking. |
| [List Project Search Engines](actions/list-project-search-engines.md) | GET | Retrieves search engine configurations for a project in SE Ranking. |
| [Update Search Engine in Project](actions/update-search-engine-in-project.md) | PUT | Updates a project search engine in SE Ranking. |

