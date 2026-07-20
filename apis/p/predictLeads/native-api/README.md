# PredictLeads: Native API Reference

A consolidated summary of PredictLeads's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.predictleads.com/api_endpoints/introduction
- **OpenAPI specification:** https://docs.predictleads.com/schemas/open_api_schema.json
- **API base URL:** `https://predictleads.com/api/v3`

## Authentication

### API Key

Authenticate with your PredictLeads API key and API token.

### Credentials

- **API Key:** `apiKey` · required
- **API Token:** `apiToken` · required · PredictLeads API token from the Your Subscription Plans page.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
X-Api-Token: <apiToken>
```

[Official authentication documentation](https://docs.predictleads.com/api_endpoints/introduction/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Follow Company](actions/follow-company.md) | `POST /companies/:company_id_or_domain/follow` | [docs](https://docs.predictleads.com/api_endpoints/follow_companies/follow_the_company) |
| [Get Company](actions/get-company.md) | `GET /companies/:id_or_domain` | [docs](https://docs.predictleads.com/api_endpoints/companies_dataset/retrieve_company) |
| [Get Job Opening](actions/get-job-opening.md) | `GET /job_openings/:id` | [docs](https://docs.predictleads.com/api_endpoints/job_openings_dataset/retrieve_a_single_job_opening_by_id) |
| [Get News Event](actions/get-news-event.md) | `GET /news_events/:id` | [docs](https://docs.predictleads.com/api_endpoints/news_events_dataset/retrieve_a_single_news_event_by_id) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://docs.predictleads.com/api_endpoints/products_dataset/retrieve_a_single_product_by_id) |
| [Get Technology](actions/get-technology.md) | `GET /technologies/:id_or_fuzzy_name` | [docs](https://docs.predictleads.com/api_endpoints/technologies_dataset/retrieve_a_single_technology_by_id_or_fuzzy_name) |
| [List Companies](actions/list-companies.md) | `GET /discover/companies` | [docs](https://docs.predictleads.com/api_endpoints/companies_dataset/retrieve_companies) |
| [List Company Connections](actions/list-company-connections.md) | `GET /companies/:company_id_or_domain/connections` | [docs](https://docs.predictleads.com/api_endpoints/connections_dataset/retrieve_company_s_connections) |
| [List Company Financing Events](actions/list-company-financing-events.md) | `GET /companies/:company_id_or_domain/financing_events` | [docs](https://docs.predictleads.com/api_endpoints/financing_events_dataset/retrieve_company_s_financing_events) |
| [List Company GitHub Repositories](actions/list-company-git-hub-repositories.md) | `GET /companies/:company_id_or_domain/github_repositories` | [docs](https://docs.predictleads.com/api_endpoints/github_repositories_dataset/retrieve_company_s_github_repositories) |
| [List Company Job Openings](actions/list-company-job-openings.md) | `GET /companies/:company_id_or_domain/job_openings` | [docs](https://docs.predictleads.com/api_endpoints/job_openings_dataset/retrieve_company_s_job_openings) |
| [List Company News Events](actions/list-company-news-events.md) | `GET /companies/:company_id_or_domain/news_events` | [docs](https://docs.predictleads.com/api_endpoints/news_events_dataset/retrieve_company_s_news_events) |
| [List Company Products](actions/list-company-products.md) | `GET /companies/:company_id_or_domain/products` | [docs](https://docs.predictleads.com/api_endpoints/products_dataset/retrieve_company_s_products) |
| [List Company Technologies](actions/list-company-technologies.md) | `GET /companies/:company_id_or_domain/technology_detections` | [docs](https://docs.predictleads.com/api_endpoints/technology_detections_dataset/retrieve_technologies_used_by_specific_company) |
| [List Company Website Evolution](actions/list-company-website-evolution.md) | `GET /companies/:company_id_or_domain/website_evolution` | [docs](https://docs.predictleads.com/api_endpoints/website_evolution_dataset/retrieve_company_s_website_evolution) |
| [List Financing Events](actions/list-financing-events.md) | `GET /discover/financing_events` | [docs](https://docs.predictleads.com/api_endpoints/financing_events_dataset/retrieve_financing_events) |
| [List Followed Companies](actions/list-followed-companies.md) | `GET /followings` | [docs](https://docs.predictleads.com/api_endpoints/follow_companies/retrieve_followed_companies) |
| [List Job Openings](actions/list-job-openings.md) | `GET /discover/job_openings` | [docs](https://docs.predictleads.com/api_endpoints/job_openings_dataset/retrieve_a_list_of_job_openings) |
| [List News Events](actions/list-news-events.md) | `GET /discover/news_events` | [docs](https://docs.predictleads.com/api_endpoints/news_events_dataset/retrieve_news_events) |
| [List Portfolio Companies](actions/list-portfolio-companies.md) | `GET /discover/portfolio_companies/connections` | [docs](https://docs.predictleads.com/api_endpoints/connections_dataset/retrieve_portfolio_companies) |
| [List Products](actions/list-products.md) | `GET /discover/products/latest` | [docs](https://docs.predictleads.com/api_endpoints/products_dataset/retrieve_a_list_of_products) |
| [List Similar Companies](actions/list-similar-companies.md) | `GET /companies/:company_id_or_domain/similar_companies` | [docs](https://docs.predictleads.com/api_endpoints/similar_companies_dataset/retrieve_company_s_similar_companies) |
| [List Startup Platform Posts](actions/list-startup-platform-posts.md) | `GET /discover/startup_platform_posts` | [docs](https://docs.predictleads.com/api_endpoints/startup_platform_posts_dataset/retrieve_latest_posts) |
| [List Technologies](actions/list-technologies.md) | `GET /technologies` | [docs](https://docs.predictleads.com/api_endpoints/technologies_dataset/retrieve_all_tracked_technologies) |
| [List Technology Companies](actions/list-technology-companies.md) | `GET /discover/technologies/:technology_id_or_fuzzy_name/technology_detections` | [docs](https://docs.predictleads.com/api_endpoints/technology_detections_dataset/retrieve_companies_using_specific_technology_id_or_fuzzy_name) |
| [Retrieve API Subscription Information](actions/retrieve-api-subscription-information.md) | `GET /api_subscription` | [docs](https://docs.predictleads.com/api_endpoints/api_subscription/retrieve_api_subscription_information) |
| [Unfollow Company](actions/unfollow-company.md) | `POST /companies/:company_id_or_domain/unfollow` | [docs](https://docs.predictleads.com/api_endpoints/follow_companies/unfollow_the_company) |
