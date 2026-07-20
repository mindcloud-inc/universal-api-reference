# <img src="https://images.mindcloud.co/apps/icons/favicon-scrape-do-48x48_1777036992672.png" alt="Scrape do logo" width="28" height="28"> Scrape do: Universal API

Scrape.do is a web scraping API for fetching raw webpages, structured search results, Google Trends data, Amazon marketplace data, and asynchronous scraping jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeDo/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrape.do/
- **Vendor API docs:** https://scrape.do/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get usage statistics](actions/get-usage-statistics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-usage-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Amazon Html

| Action | Method | Description |
| --- | --- | --- |
| [Get Amazon raw HTML](actions/get-amazon-raw-html.md) | GET | Retrieves Amazon raw HTML with Scrape do. |

### Amazon Offers

| Action | Method | Description |
| --- | --- | --- |
| [Get Amazon offers](actions/get-amazon-offers.md) | GET | Retrieves Amazon offers with Scrape do. |

### Amazon Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Amazon product details](actions/get-amazon-product-details.md) | GET | Retrieves Amazon product details with Scrape do. |
| [Search Amazon products](actions/search-amazon-products.md) | GET | Finds Amazon products with Scrape do. |

### Async Account

| Action | Method | Description |
| --- | --- | --- |
| [Get async user info](actions/get-async-user-info.md) | GET | Retrieves async user information from Scrape do. |

### Async Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel async job](actions/cancel-async-job.md) | DELETE | Cancels an async job in Scrape do. |
| [Create async scraping job](actions/create-async-scraping-job.md) | POST | Creates a new async scraping job in Scrape do. |
| [Get async job details](actions/get-async-job-details.md) | GET | Retrieves async job details from Scrape do. |
| [List async jobs](actions/list-async-jobs.md) | GET | Retrieves async jobs from Scrape do. |

### Async Task

| Action | Method | Description |
| --- | --- | --- |
| [Get async task details](actions/get-async-task-details.md) | GET | Retrieves async task details from Scrape do. |

### Google Ai Mode

| Action | Method | Description |
| --- | --- | --- |
| [Use Google AI mode](actions/use-google-ai-mode.md) | GET | Retrieves Google AI Mode results with Scrape do. |

### Google Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search Google](actions/search-google.md) | GET | Finds Google search results with Scrape do. |

### Google Trending Now

| Action | Method | Description |
| --- | --- | --- |
| [Get Google trending now](actions/get-google-trending-now.md) | GET | Retrieves Google trending searches with Scrape do. |

### Google Trends

| Action | Method | Description |
| --- | --- | --- |
| [Get Google trends data](actions/get-google-trends-data.md) | GET | Retrieves Google Trends data with Scrape do. |

### Http Response

| Action | Method | Description |
| --- | --- | --- |
| [Send DELETE request](actions/send-delete-request.md) | DELETE | Sends a DELETE request with Scrape do. |
| [Send PATCH request](actions/send-patch-request.md) | PUT | Sends a PATCH request with Scrape do. |
| [Send POST request](actions/send-post-request.md) | POST | Sends a POST request with Scrape do. |
| [Send PUT request](actions/send-put-request.md) | PUT | Sends a PUT request with Scrape do. |

### Usage Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get usage statistics](actions/get-usage-statistics.md) | GET | Retrieves usage statistics from Scrape do. |

### Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Fetch webpage](actions/fetch-webpage.md) | GET | Retrieves webpage content with Scrape do. |

