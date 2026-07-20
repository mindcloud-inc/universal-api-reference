# <img src="https://images.mindcloud.co/apps/icons/scrape-ops_1775752025711.png" alt="ScrapeOps logo" width="28" height="28"> ScrapeOps: Universal API

Generate headers, proxy requests, and monitor and schedule scrapers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeOps/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapeops.io
- **Vendor API docs:** https://scrapeops.io/docs/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Browser Headers](actions/list-browser-headers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-browser-headers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Amazon Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Amazon Product](actions/get-amazon-product.md) | GET | Retrieves Amazon product data from ScrapeOps. |

### Amazon Product Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Amazon Products](actions/search-amazon-products.md) | GET | Retrieves Amazon search results from ScrapeOps. |

### Browser Header

| Action | Method | Description |
| --- | --- | --- |
| [List Browser Headers](actions/list-browser-headers.md) | GET | Retrieves fake browser headers from ScrapeOps. |

### Ebay Category

| Action | Method | Description |
| --- | --- | --- |
| [List Ebay Categories](actions/list-ebay-categories.md) | GET | Retrieves eBay category data from ScrapeOps. |

### Ebay Feedback

| Action | Method | Description |
| --- | --- | --- |
| [List Ebay Feedback](actions/list-ebay-feedback.md) | GET | Retrieves eBay feedback from ScrapeOps. |

### Ebay Listing Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Ebay Listings](actions/search-ebay-listings.md) | GET | Retrieves eBay search results from ScrapeOps. |

### Ebay Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Ebay Product](actions/get-ebay-product.md) | GET | Retrieves eBay product data from ScrapeOps. |

### Ebay Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Ebay Store](actions/get-ebay-store.md) | GET | Retrieves eBay store data from ScrapeOps. |

### Indeed Company Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Indeed Companies](actions/search-indeed-companies.md) | GET | Retrieves Indeed company search results from ScrapeOps. |

### Indeed Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Indeed Job](actions/get-indeed-job.md) | GET | Retrieves Indeed job details from ScrapeOps. |

### Indeed Job Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Indeed Jobs](actions/search-indeed-jobs.md) | GET | Retrieves Indeed job search results from ScrapeOps. |

### Parsed Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch And Parse Url With Custom Parser](actions/fetch-and-parse-url-with-custom-parser.md) | GET | Fetches and parses a URL with a ScrapeOps custom parser. |
| [Parse Html With Custom Parser](actions/parse-html-with-custom-parser.md) | GET | Parses HTML with a ScrapeOps custom parser. |

### Proxy Response

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Url Via Proxy Api Aggregator](actions/fetch-url-via-proxy-api-aggregator.md) | GET | Fetches a URL through the ScrapeOps proxy aggregator. |

### Scheduled Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduled Job](actions/create-scheduled-job.md) | POST | Creates a scheduled job in ScrapeOps. |
| [Delete Scheduled Job](actions/delete-scheduled-job.md) | DELETE | Deletes a scheduled job from ScrapeOps. |
| [List All Scheduled Jobs](actions/list-all-scheduled-jobs.md) | GET | Retrieves scheduled jobs from ScrapeOps. |

### Server

| Action | Method | Description |
| --- | --- | --- |
| [List Servers](actions/list-servers.md) | GET | Retrieves scraper servers from ScrapeOps. |

### Spider

| Action | Method | Description |
| --- | --- | --- |
| [List Spiders By Server Id](actions/list-spiders-by-server-id.md) | GET | Retrieves spiders for a ScrapeOps server. |

### Spider Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Spider](actions/run-spider.md) | POST | Runs a spider on a ScrapeOps server. |

### User Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Fake User Agents](actions/list-fake-user-agents.md) | GET | Retrieves fake user agents from ScrapeOps. |

### Walmart Browse Result

| Action | Method | Description |
| --- | --- | --- |
| [Browse Walmart Products](actions/browse-walmart-products.md) | GET | Retrieves Walmart browse results from ScrapeOps. |

### Walmart Category

| Action | Method | Description |
| --- | --- | --- |
| [List Walmart Categories](actions/list-walmart-categories.md) | GET | Retrieves Walmart category data from ScrapeOps. |

### Walmart Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Walmart Product](actions/get-walmart-product.md) | GET | Retrieves Walmart product data from ScrapeOps. |

### Walmart Product Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Walmart Products](actions/search-walmart-products.md) | GET | Retrieves Walmart search results from ScrapeOps. |

### Walmart Review

| Action | Method | Description |
| --- | --- | --- |
| [List Walmart Reviews](actions/list-walmart-reviews.md) | GET | Retrieves Walmart reviews from ScrapeOps. |

### Walmart Shop Result

| Action | Method | Description |
| --- | --- | --- |
| [List Walmart Shop Results](actions/list-walmart-shop-results.md) | GET | Retrieves Walmart shop results from ScrapeOps. |

