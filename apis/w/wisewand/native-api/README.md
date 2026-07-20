# Wisewand: Native API Reference

A consolidated summary of Wisewand's API configuration and 83 documented operations, with links to official documentation.

- **Official docs:** https://api.wisewand.ai/docs
- **OpenAPI specification:** https://api.wisewand.ai/docs/json
- **API base URL:** `https://api.wisewand.ai`

## Authentication

### API Key

Authenticate with your Wisewand API key using the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.wisewand.ai/docs)

## Pagination

Use `take` in the query string to set the page size (default 20; accepted range 1–50). Use `skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (83 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create a feed](actions/create-a-feed.md) | `POST /v1/feeds/` | [docs](https://api.wisewand.ai/docs) |
| [Create and run a articles](actions/create-and-run-a-articles.md) | `POST /v1/articles/` | [docs](https://api.wisewand.ai/docs) |
| [Create and run a categorypages](actions/create-and-run-a-categorypages.md) | `POST /v1/categorypages/` | [docs](https://api.wisewand.ai/docs) |
| [Create and run a discoverarticles](actions/create-and-run-a-discoverarticles.md) | `POST /v1/discoverarticles/` | [docs](https://api.wisewand.ai/docs) |
| [Create and run a productpages](actions/create-and-run-a-productpages.md) | `POST /v1/productpages/` | [docs](https://api.wisewand.ai/docs) |
| [Create and run a updateposts](actions/create-and-run-a-updateposts.md) | `POST /v1/updateposts/` | [docs](https://api.wisewand.ai/docs) |
| [Create connections](actions/create-connections.md) | `POST /v1/connections/` | [docs](https://api.wisewand.ai/docs) |
| [Create multiple articles](actions/create-multiple-articles.md) | `POST /v1/articles/bulk` | [docs](https://api.wisewand.ai/docs) |
| [Create multiple categorypages](actions/create-multiple-categorypages.md) | `POST /v1/categorypages/bulk` | [docs](https://api.wisewand.ai/docs) |
| [Create multiple discoverarticles](actions/create-multiple-discoverarticles.md) | `POST /v1/discoverarticles/bulk` | [docs](https://api.wisewand.ai/docs) |
| [Create multiple productpages](actions/create-multiple-productpages.md) | `POST /v1/productpages/bulk` | [docs](https://api.wisewand.ai/docs) |
| [Create multiple updateposts](actions/create-multiple-updateposts.md) | `POST /v1/updateposts/bulk` | [docs](https://api.wisewand.ai/docs) |
| [Create personas](actions/create-personas.md) | `POST /v1/personas/` | [docs](https://api.wisewand.ai/docs) |
| [Create projects](actions/create-projects.md) | `POST /v1/projects/` | [docs](https://api.wisewand.ai/docs) |
| [Delete connections](actions/delete-connections.md) | `DELETE /v1/connections/:id` | [docs](https://api.wisewand.ai/docs) |
| [Delete personas](actions/delete-personas.md) | `DELETE /v1/personas/:id` | [docs](https://api.wisewand.ai/docs) |
| [Delete projects](actions/delete-projects.md) | `DELETE /v1/projects/:id` | [docs](https://api.wisewand.ai/docs) |
| [Deletev1feedsbyid](actions/deletev1feedsbyid.md) | `DELETE /v1/feeds/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get a articles](actions/get-a-articles.md) | `GET /v1/articles/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get a categorypages](actions/get-a-categorypages.md) | `GET /v1/categorypages/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get a discoverarticles](actions/get-a-discoverarticles.md) | `GET /v1/discoverarticles/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get a feeds](actions/get-a-feeds.md) | `GET /v1/feeds/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get a productpages](actions/get-a-productpages.md) | `GET /v1/productpages/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get a updateposts](actions/get-a-updateposts.md) | `GET /v1/updateposts/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get all authors](actions/get-all-authors.md) | `GET /v1/authors/` | [docs](https://api.wisewand.ai/docs) |
| [Get all categories](actions/get-all-categories.md) | `GET /v1/categories/` | [docs](https://api.wisewand.ai/docs) |
| [Get connections](actions/get-connections.md) | `GET /v1/connections/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get daily summary of transactions](actions/get-daily-summary-of-transactions.md) | `GET /v1/transactions/daily` | [docs](https://api.wisewand.ai/docs) |
| [Get entity counts summary](actions/get-entity-counts-summary.md) | `GET /v1/entities/summary/` | [docs](https://api.wisewand.ai/docs) |
| [Get job status](actions/get-job-status.md) | `GET /v1/jobs/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get personas](actions/get-personas.md) | `GET /v1/personas/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get projects](actions/get-projects.md) | `GET /v1/projects/:id` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating multiple articles](actions/get-the-cost-of-creating-multiple-articles.md) | `POST /v1/articles/bulk/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating multiple categorypages](actions/get-the-cost-of-creating-multiple-categorypages.md) | `POST /v1/categorypages/bulk/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating multiple discoverarticles](actions/get-the-cost-of-creating-multiple-discoverarticles.md) | `POST /v1/discoverarticles/bulk/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating multiple productpages](actions/get-the-cost-of-creating-multiple-productpages.md) | `POST /v1/productpages/bulk/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating multiple updateposts](actions/get-the-cost-of-creating-multiple-updateposts.md) | `POST /v1/updateposts/bulk/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating one articles](actions/get-the-cost-of-creating-one-articles.md) | `POST /v1/articles/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating one categorypages](actions/get-the-cost-of-creating-one-categorypages.md) | `POST /v1/categorypages/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating one discoverarticles](actions/get-the-cost-of-creating-one-discoverarticles.md) | `POST /v1/discoverarticles/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating one productpages](actions/get-the-cost-of-creating-one-productpages.md) | `POST /v1/productpages/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the cost of creating one updateposts](actions/get-the-cost-of-creating-one-updateposts.md) | `POST /v1/updateposts/cost` | [docs](https://api.wisewand.ai/docs) |
| [Get the result of articles](actions/get-the-result-of-articles.md) | `GET /v1/articles/:id/output` | [docs](https://api.wisewand.ai/docs) |
| [Get the result of categorypages](actions/get-the-result-of-categorypages.md) | `GET /v1/categorypages/:id/output` | [docs](https://api.wisewand.ai/docs) |
| [Get the result of discoverarticles](actions/get-the-result-of-discoverarticles.md) | `GET /v1/discoverarticles/:id/output` | [docs](https://api.wisewand.ai/docs) |
| [Get the result of productpages](actions/get-the-result-of-productpages.md) | `GET /v1/productpages/:id/output` | [docs](https://api.wisewand.ai/docs) |
| [Get the result of updateposts](actions/get-the-result-of-updateposts.md) | `GET /v1/updateposts/:id/output` | [docs](https://api.wisewand.ai/docs) |
| [List articles](actions/list-articles.md) | `GET /v1/articles/` | [docs](https://api.wisewand.ai/docs) |
| [List categorypages](actions/list-categorypages.md) | `GET /v1/categorypages/` | [docs](https://api.wisewand.ai/docs) |
| [List connections](actions/list-connections.md) | `GET /v1/connections/` | [docs](https://api.wisewand.ai/docs) |
| [List discoverarticles](actions/list-discoverarticles.md) | `GET /v1/discoverarticles/` | [docs](https://api.wisewand.ai/docs) |
| [List feeds](actions/list-feeds.md) | `GET /v1/feeds/` | [docs](https://api.wisewand.ai/docs) |
| [List personas](actions/list-personas.md) | `GET /v1/personas/` | [docs](https://api.wisewand.ai/docs) |
| [List productpages](actions/list-productpages.md) | `GET /v1/productpages/` | [docs](https://api.wisewand.ai/docs) |
| [List projects](actions/list-projects.md) | `GET /v1/projects/` | [docs](https://api.wisewand.ai/docs) |
| [List transactions](actions/list-transactions.md) | `GET /v1/transactions/` | [docs](https://api.wisewand.ai/docs) |
| [List updateposts](actions/list-updateposts.md) | `GET /v1/updateposts/` | [docs](https://api.wisewand.ai/docs) |
| [Publish entity to Prestashop](actions/publish-entity-to-prestashop.md) | `POST /v1/publish/prestashop/:entity_id` | [docs](https://api.wisewand.ai/docs) |
| [Publish entity to Shopify](actions/publish-entity-to-shopify.md) | `POST /v1/publish/shopify/:entity_id` | [docs](https://api.wisewand.ai/docs) |
| [Publish entity to webhook](actions/publish-entity-to-webhook.md) | `POST /v1/publish/webhook/:entity_id` | [docs](https://api.wisewand.ai/docs) |
| [Publish entity to WooCommerce](actions/publish-entity-to-woocommerce.md) | `POST /v1/publish/woocommerce/:entity_id` | [docs](https://api.wisewand.ai/docs) |
| [Publish entity to WordPress](actions/publish-entity-to-wordpress.md) | `POST /v1/publish/wordpress/:entity_id` | [docs](https://api.wisewand.ai/docs) |
| [Run a articles](actions/run-a-articles.md) | `POST /v1/articles/:id/run` | [docs](https://api.wisewand.ai/docs) |
| [Run a categorypages](actions/run-a-categorypages.md) | `POST /v1/categorypages/:id/run` | [docs](https://api.wisewand.ai/docs) |
| [Run a discoverarticles](actions/run-a-discoverarticles.md) | `POST /v1/discoverarticles/:id/run` | [docs](https://api.wisewand.ai/docs) |
| [Run a productpages](actions/run-a-productpages.md) | `POST /v1/productpages/:id/run` | [docs](https://api.wisewand.ai/docs) |
| [Run a updateposts](actions/run-a-updateposts.md) | `POST /v1/updateposts/:id/run` | [docs](https://api.wisewand.ai/docs) |
| [Trigger a job](actions/trigger-a-job.md) | `POST /v1/jobs/:name` | [docs](https://api.wisewand.ai/docs) |
| [Update a articles](actions/update-a-articles.md) | `PATCH /v1/articles/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update a categorypages](actions/update-a-categorypages.md) | `PATCH /v1/categorypages/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update a discoverarticles](actions/update-a-discoverarticles.md) | `PATCH /v1/discoverarticles/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update a feeds](actions/update-a-feeds.md) | `PATCH /v1/feeds/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update a productpages](actions/update-a-productpages.md) | `PATCH /v1/productpages/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update a updateposts](actions/update-a-updateposts.md) | `PATCH /v1/updateposts/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update connections](actions/update-connections.md) | `PATCH /v1/connections/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update personas](actions/update-personas.md) | `PATCH /v1/personas/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update projects](actions/update-projects.md) | `PATCH /v1/projects/:id` | [docs](https://api.wisewand.ai/docs) |
| [Update the result of articles](actions/update-the-result-of-articles.md) | `PATCH /v1/articles/:id/output/:outputId` | [docs](https://api.wisewand.ai/docs) |
| [Update the result of categorypages](actions/update-the-result-of-categorypages.md) | `PATCH /v1/categorypages/:id/output/:outputId` | [docs](https://api.wisewand.ai/docs) |
| [Update the result of discoverarticles](actions/update-the-result-of-discoverarticles.md) | `PATCH /v1/discoverarticles/:id/output/:outputId` | [docs](https://api.wisewand.ai/docs) |
| [Update the result of productpages](actions/update-the-result-of-productpages.md) | `PATCH /v1/productpages/:id/output/:outputId` | [docs](https://api.wisewand.ai/docs) |
| [Update the result of updateposts](actions/update-the-result-of-updateposts.md) | `PATCH /v1/updateposts/:id/output/:outputId` | [docs](https://api.wisewand.ai/docs) |
