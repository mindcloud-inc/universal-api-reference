# <img src="https://images.mindcloud.co/apps/icons/wisewand-icon-square_1776107001920.png" alt="Wisewand logo" width="28" height="28"> Wisewand: Universal API

Wisewand is an AI SEO content platform for generating, managing, and publishing articles, product pages, category pages, discovery articles, and update posts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wisewand/latest
- **Category:** Marketing
- **Actions:** 83
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wisewand.ai
- **Vendor API docs:** https://api.wisewand.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (83)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create and run a articles](actions/create-and-run-a-articles.md) | POST | Creates and runs an article in Wisewand. |
| [Create multiple articles](actions/create-multiple-articles.md) | POST | Creates multiple new articles in Wisewand. |
| [Get a articles](actions/get-a-articles.md) | GET | Retrieves an article from your Wisewand workspace. |
| [Get the cost of creating multiple articles](actions/get-the-cost-of-creating-multiple-articles.md) | POST | Retrieves bulk article creation cost from Wisewand. |
| [Get the cost of creating one articles](actions/get-the-cost-of-creating-one-articles.md) | POST | Retrieves article creation cost from Wisewand. |
| [Get the result of articles](actions/get-the-result-of-articles.md) | GET | Retrieves an article result from Wisewand. |
| [List articles](actions/list-articles.md) | GET | Retrieves articles from your Wisewand workspace. |
| [Run a articles](actions/run-a-articles.md) | POST | Runs an article job in Wisewand. |
| [Update a articles](actions/update-a-articles.md) | PUT | Updates an existing article in your Wisewand workspace. |
| [Update the result of articles](actions/update-the-result-of-articles.md) | PUT | Updates an article result in Wisewand. |

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Get all authors](actions/get-all-authors.md) | GET | Retrieves authors from your Wisewand workspace. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get all categories](actions/get-all-categories.md) | GET | Retrieves categories from your Wisewand workspace. |

### Category Page

| Action | Method | Description |
| --- | --- | --- |
| [Create and run a categorypages](actions/create-and-run-a-categorypages.md) | POST | Creates and runs a category page in Wisewand. |
| [Create multiple categorypages](actions/create-multiple-categorypages.md) | POST | Creates multiple new category pages in Wisewand. |
| [Get a categorypages](actions/get-a-categorypages.md) | GET | Retrieves a category page from your Wisewand workspace. |
| [Get the cost of creating multiple categorypages](actions/get-the-cost-of-creating-multiple-categorypages.md) | POST | Retrieves bulk category page creation cost from Wisewand. |
| [Get the cost of creating one categorypages](actions/get-the-cost-of-creating-one-categorypages.md) | POST | Retrieves category page creation cost from Wisewand. |
| [Get the result of categorypages](actions/get-the-result-of-categorypages.md) | GET | Retrieves a category page result from Wisewand. |
| [List categorypages](actions/list-categorypages.md) | GET | Retrieves category pages from your Wisewand workspace. |
| [Run a categorypages](actions/run-a-categorypages.md) | POST | Runs a category page in Wisewand. |
| [Update a categorypages](actions/update-a-categorypages.md) | PUT | Updates an existing category page in your Wisewand workspace. |
| [Update the result of categorypages](actions/update-the-result-of-categorypages.md) | PUT | Updates a category page result in Wisewand. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Create connections](actions/create-connections.md) | POST | Creates a new connection in your Wisewand workspace. |
| [Delete connections](actions/delete-connections.md) | DELETE | Deletes an existing connection from your Wisewand workspace. |
| [Get connections](actions/get-connections.md) | GET | Retrieves a connection from your Wisewand workspace. |
| [List connections](actions/list-connections.md) | GET | Retrieves connections from your Wisewand workspace. |
| [Update connections](actions/update-connections.md) | PUT | Updates an existing connection in your Wisewand workspace. |

### Discover Article

| Action | Method | Description |
| --- | --- | --- |
| [Create and run a discoverarticles](actions/create-and-run-a-discoverarticles.md) | POST | Creates and runs a discovery article in Wisewand. |
| [Create multiple discoverarticles](actions/create-multiple-discoverarticles.md) | POST | Creates multiple new discovery articles in Wisewand. |
| [Get a discoverarticles](actions/get-a-discoverarticles.md) | GET | Retrieves a discovery article from your Wisewand workspace. |
| [Get the cost of creating multiple discoverarticles](actions/get-the-cost-of-creating-multiple-discoverarticles.md) | POST | Retrieves bulk discovery article creation cost from Wisewand. |
| [Get the cost of creating one discoverarticles](actions/get-the-cost-of-creating-one-discoverarticles.md) | POST | Retrieves discovery article creation cost from Wisewand. |
| [Get the result of discoverarticles](actions/get-the-result-of-discoverarticles.md) | GET | Retrieves a discovery article result from Wisewand. |
| [List discoverarticles](actions/list-discoverarticles.md) | GET | Retrieves discovery articles from your Wisewand workspace. |
| [Run a discoverarticles](actions/run-a-discoverarticles.md) | POST | Runs a discovery article in Wisewand. |
| [Update a discoverarticles](actions/update-a-discoverarticles.md) | PUT | Updates an existing discovery article in your Wisewand workspace. |
| [Update the result of discoverarticles](actions/update-the-result-of-discoverarticles.md) | PUT | Updates a discovery article result in Wisewand. |

### Entity Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get entity counts summary](actions/get-entity-counts-summary.md) | GET | Retrieves entity count summaries from your Wisewand workspace. |

### Feed

| Action | Method | Description |
| --- | --- | --- |
| [Create a feed](actions/create-a-feed.md) | POST | Creates a new feed in your Wisewand workspace. |
| [Deletev1feedsbyid](actions/deletev1feedsbyid.md) | DELETE | Deletes an existing feed from your Wisewand workspace. |
| [Get a feeds](actions/get-a-feeds.md) | GET | Retrieves a feed from your Wisewand workspace. |
| [List feeds](actions/list-feeds.md) | GET | Retrieves feeds from your Wisewand workspace. |
| [Update a feeds](actions/update-a-feeds.md) | PUT | Updates an existing feed in your Wisewand workspace. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get job status](actions/get-job-status.md) | GET | Retrieves a job status from your Wisewand workspace. |
| [Trigger a job](actions/trigger-a-job.md) | POST | Triggers a job in your Wisewand workspace. |

### Persona

| Action | Method | Description |
| --- | --- | --- |
| [Create personas](actions/create-personas.md) | POST | Creates a new persona in your Wisewand workspace. |
| [Delete personas](actions/delete-personas.md) | DELETE | Deletes an existing persona from your Wisewand workspace. |
| [Get personas](actions/get-personas.md) | GET | Retrieves a persona from your Wisewand workspace. |
| [List personas](actions/list-personas.md) | GET | Retrieves personas from your Wisewand workspace. |
| [Update personas](actions/update-personas.md) | PUT | Updates an existing persona in your Wisewand workspace. |

### Product Page

| Action | Method | Description |
| --- | --- | --- |
| [Create and run a productpages](actions/create-and-run-a-productpages.md) | POST | Creates and runs a product page in Wisewand. |
| [Create multiple productpages](actions/create-multiple-productpages.md) | POST | Creates multiple new product pages in Wisewand. |
| [Get a productpages](actions/get-a-productpages.md) | GET | Retrieves a product page from your Wisewand workspace. |
| [Get the cost of creating multiple productpages](actions/get-the-cost-of-creating-multiple-productpages.md) | POST | Retrieves bulk product page creation cost from Wisewand. |
| [Get the cost of creating one productpages](actions/get-the-cost-of-creating-one-productpages.md) | POST | Retrieves product page creation cost from Wisewand. |
| [Get the result of productpages](actions/get-the-result-of-productpages.md) | GET | Retrieves a product page result from Wisewand. |
| [List productpages](actions/list-productpages.md) | GET | Retrieves product pages from your Wisewand workspace. |
| [Run a productpages](actions/run-a-productpages.md) | POST | Runs a product page in Wisewand. |
| [Update a productpages](actions/update-a-productpages.md) | PUT | Updates an existing product page in your Wisewand workspace. |
| [Update the result of productpages](actions/update-the-result-of-productpages.md) | PUT | Updates a product page result in Wisewand. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create projects](actions/create-projects.md) | POST | Creates a new project in your Wisewand workspace. |
| [Delete projects](actions/delete-projects.md) | DELETE | Deletes an existing project from your Wisewand workspace. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your Wisewand workspace. |
| [Get projects](actions/get-projects.md) | GET | Retrieves a project from your Wisewand workspace. |
| [List projects](actions/list-projects.md) | GET | Retrieves projects from your Wisewand workspace. |
| [Update projects](actions/update-projects.md) | PUT | Updates an existing project in your Wisewand workspace. |

### Publication

| Action | Method | Description |
| --- | --- | --- |
| [Publish entity to Prestashop](actions/publish-entity-to-prestashop.md) | POST | Publishes a Wisewand entity to Prestashop. |
| [Publish entity to Shopify](actions/publish-entity-to-shopify.md) | POST | Publishes a Wisewand entity to Shopify. |
| [Publish entity to webhook](actions/publish-entity-to-webhook.md) | POST | Publishes a Wisewand entity to a webhook. |
| [Publish entity to WooCommerce](actions/publish-entity-to-woocommerce.md) | POST | Publishes a Wisewand entity to WooCommerce. |
| [Publish entity to WordPress](actions/publish-entity-to-wordpress.md) | POST | Publishes a Wisewand entity to WordPress. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get daily summary of transactions](actions/get-daily-summary-of-transactions.md) | GET | Retrieves daily transaction summaries from your Wisewand workspace. |
| [List transactions](actions/list-transactions.md) | GET | Retrieves transactions from your Wisewand workspace. |

### Update Post

| Action | Method | Description |
| --- | --- | --- |
| [Create and run a updateposts](actions/create-and-run-a-updateposts.md) | POST | Creates and runs an update post in Wisewand. |
| [Create multiple updateposts](actions/create-multiple-updateposts.md) | POST | Creates multiple new update posts in Wisewand. |
| [Get a updateposts](actions/get-a-updateposts.md) | GET | Retrieves an update post from your Wisewand workspace. |
| [Get the cost of creating multiple updateposts](actions/get-the-cost-of-creating-multiple-updateposts.md) | POST | Retrieves bulk update post creation cost from Wisewand. |
| [Get the cost of creating one updateposts](actions/get-the-cost-of-creating-one-updateposts.md) | POST | Retrieves update post creation cost from Wisewand. |
| [Get the result of updateposts](actions/get-the-result-of-updateposts.md) | GET | Retrieves an update post result from Wisewand. |
| [List updateposts](actions/list-updateposts.md) | GET | Retrieves update posts from your Wisewand workspace. |
| [Run a updateposts](actions/run-a-updateposts.md) | POST | Runs an update post in Wisewand. |
| [Update a updateposts](actions/update-a-updateposts.md) | PUT | Updates an existing update post in your Wisewand workspace. |
| [Update the result of updateposts](actions/update-the-result-of-updateposts.md) | PUT | Updates an update post result in Wisewand. |

