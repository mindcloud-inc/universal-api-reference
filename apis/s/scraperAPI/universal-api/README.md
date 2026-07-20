# <img src="https://images.mindcloud.co/apps/icons/scraper-api_1775758704275.png" alt="ScraperAPI logo" width="28" height="28"> ScraperAPI: Universal API

Scrape pages, run jobs, and extract structured web data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scraperAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scraperapi.com
- **Vendor API docs:** https://docs.scraperapi.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List DataPipeline Projects](actions/list-data-pipeline-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Async Job](actions/cancel-async-job.md) | DELETE | Cancels an async scraping job in ScraperAPI. |
| [Cancel DataPipeline Project Job](actions/cancel-data-pipeline-project-job.md) | DELETE | Cancels a DataPipeline project job in ScraperAPI. |
| [Create Async Batch Jobs](actions/create-async-batch-jobs.md) | POST | Creates async batch scraping jobs in ScraperAPI. |
| [Create Async Job](actions/create-async-job.md) | POST | Creates an async scraping job in ScraperAPI. |
| [Get Async Job](actions/get-async-job.md) | GET | Retrieves an async scraping job from ScraperAPI. |
| [List DataPipeline Project Jobs](actions/list-data-pipeline-project-jobs.md) | GET | Retrieves DataPipeline project jobs from ScraperAPI. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Page](actions/scrape-page.md) | GET | Retrieves a scraped page from ScraperAPI. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Archive DataPipeline Project](actions/archive-data-pipeline-project.md) | DELETE | Archives an existing DataPipeline project in ScraperAPI. |
| [Create Amazon Offers DataPipeline Project](actions/create-amazon-offers-data-pipeline-project.md) | POST | Creates an Amazon offers DataPipeline project in ScraperAPI. |
| [Create Amazon Product DataPipeline Project](actions/create-amazon-product-data-pipeline-project.md) | POST | Creates an Amazon product DataPipeline project in ScraperAPI. |
| [Create Amazon Reviews DataPipeline Project](actions/create-amazon-reviews-data-pipeline-project.md) | POST | Creates an Amazon reviews DataPipeline project in ScraperAPI. |
| [Create Amazon Search DataPipeline Project](actions/create-amazon-search-data-pipeline-project.md) | POST | Creates an Amazon search DataPipeline project in ScraperAPI. |
| [Create eBay Product DataPipeline Project](actions/create-ebay-product-data-pipeline-project.md) | POST | Creates an eBay product DataPipeline project in ScraperAPI. |
| [Create eBay Search DataPipeline Project](actions/create-ebay-search-data-pipeline-project.md) | POST | Creates an eBay search DataPipeline project in ScraperAPI. |
| [Create Google Jobs DataPipeline Project](actions/create-google-jobs-data-pipeline-project.md) | POST | Creates a Google Jobs DataPipeline project in ScraperAPI. |
| [Create Google News DataPipeline Project](actions/create-google-news-data-pipeline-project.md) | POST | Creates a Google News DataPipeline project in ScraperAPI. |
| [Create Google Search DataPipeline Project](actions/create-google-search-data-pipeline-project.md) | POST | Creates a Google Search DataPipeline project in ScraperAPI. |
| [Create Google Shopping DataPipeline Project](actions/create-google-shopping-data-pipeline-project.md) | POST | Creates a Google Shopping DataPipeline project in ScraperAPI. |
| [Create Redfin Agent DataPipeline Project](actions/create-redfin-agent-data-pipeline-project.md) | POST | Creates a Redfin agent DataPipeline project in ScraperAPI. |
| [Create Redfin For Rent DataPipeline Project](actions/create-redfin-for-rent-data-pipeline-project.md) | POST | Creates a Redfin for-rent DataPipeline project in ScraperAPI. |
| [Create Redfin For Sale DataPipeline Project](actions/create-redfin-for-sale-data-pipeline-project.md) | POST | Creates a Redfin for-sale DataPipeline project in ScraperAPI. |
| [Create Redfin Search DataPipeline Project](actions/create-redfin-search-data-pipeline-project.md) | POST | Creates a Redfin search DataPipeline project in ScraperAPI. |
| [Create URL DataPipeline Project](actions/create-url-data-pipeline-project.md) | POST | Creates a URL DataPipeline project in ScraperAPI. |
| [Create Walmart Category DataPipeline Project](actions/create-walmart-category-data-pipeline-project.md) | POST | Creates a Walmart category DataPipeline project in ScraperAPI. |
| [Create Walmart Product DataPipeline Project](actions/create-walmart-product-data-pipeline-project.md) | POST | Creates a Walmart product DataPipeline project in ScraperAPI. |
| [Create Walmart Review DataPipeline Project](actions/create-walmart-review-data-pipeline-project.md) | POST | Creates a Walmart review DataPipeline project in ScraperAPI. |
| [Create Walmart Search DataPipeline Project](actions/create-walmart-search-data-pipeline-project.md) | POST | Creates a Walmart search DataPipeline project in ScraperAPI. |
| [Get DataPipeline Project](actions/get-data-pipeline-project.md) | GET | Retrieves a DataPipeline project from ScraperAPI. |
| [List DataPipeline Projects](actions/list-data-pipeline-projects.md) | GET | Retrieves DataPipeline projects from ScraperAPI. |
| [Update DataPipeline Project](actions/update-data-pipeline-project.md) | PUT | Updates an existing DataPipeline project in ScraperAPI. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Send Scrape Request](actions/send-scrape-request.md) | GET | Retrieves a scraped response from ScraperAPI with a POST request. |

