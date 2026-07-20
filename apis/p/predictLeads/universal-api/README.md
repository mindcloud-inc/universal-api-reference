# <img src="https://images.mindcloud.co/apps/icons/predict-leads_1775752379621.png" alt="PredictLeads logo" width="28" height="28"> PredictLeads: Universal API

Find company signals, job openings, technologies, and business connections

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/predictLeads/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://predictleads.com
- **Vendor API docs:** https://docs.predictleads.com/api_endpoints/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve API Subscription Information](actions/retrieve-api-subscription-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/retrieve-api-subscription-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Api Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve API Subscription Information](actions/retrieve-api-subscription-information.md) | GET | Retrieves API subscription details from the PredictLeads API. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Company Financing Events](actions/list-company-financing-events.md) | GET | Retrieves financing events for a PredictLeads company. |
| [List Company Technologies](actions/list-company-technologies.md) | GET | Retrieves technologies used by a PredictLeads company. |
| [List Company Website Evolution](actions/list-company-website-evolution.md) | GET | Retrieves website evolution for a PredictLeads company. |
| [List Followed Companies](actions/list-followed-companies.md) | GET | Retrieves followed companies from the PredictLeads API. |
| [List Technology Companies](actions/list-technology-companies.md) | GET | Retrieves companies using a technology from PredictLeads. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from the PredictLeads API. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from the PredictLeads API. |
| [List Portfolio Companies](actions/list-portfolio-companies.md) | GET | Retrieves portfolio companies from the PredictLeads API. |
| [List Similar Companies](actions/list-similar-companies.md) | GET | Retrieves similar companies from the PredictLeads API. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Company Connections](actions/list-company-connections.md) | GET | Retrieves company connections from the PredictLeads API. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get News Event](actions/get-news-event.md) | GET | Retrieves a news event from the PredictLeads API. |
| [List Company News Events](actions/list-company-news-events.md) | GET | Retrieves news events for a PredictLeads company. |
| [List Financing Events](actions/list-financing-events.md) | GET | Retrieves financing events from the PredictLeads API. |
| [List News Events](actions/list-news-events.md) | GET | Retrieves news events from the PredictLeads API. |

### Job Postings

| Action | Method | Description |
| --- | --- | --- |
| [List Startup Platform Posts](actions/list-startup-platform-posts.md) | GET | Retrieves startup platform posts from the PredictLeads API. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Opening](actions/get-job-opening.md) | GET | Retrieves a job opening from the PredictLeads API. |
| [List Company Job Openings](actions/list-company-job-openings.md) | GET | Retrieves job openings for a PredictLeads company. |
| [List Job Openings](actions/list-job-openings.md) | GET | Retrieves job openings from the PredictLeads API. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Follow Company](actions/follow-company.md) | POST | Follows a company in the PredictLeads API. |
| [Get Technology](actions/get-technology.md) | GET | Retrieves a technology from the PredictLeads API. |
| [List Technologies](actions/list-technologies.md) | GET | Retrieves tracked technologies from the PredictLeads API. |
| [Unfollow Company](actions/unfollow-company.md) | DELETE | Unfollows a company in the PredictLeads API. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from the PredictLeads API. |
| [List Company Products](actions/list-company-products.md) | GET | Retrieves products for a PredictLeads company. |
| [List Products](actions/list-products.md) | GET | Retrieves products from the PredictLeads API. |

### Repositories

| Action | Method | Description |
| --- | --- | --- |
| [List Company GitHub Repositories](actions/list-company-git-hub-repositories.md) | GET | Retrieves GitHub repositories for a PredictLeads company. |

