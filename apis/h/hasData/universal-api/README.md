# <img src="https://images.mindcloud.co/apps/icons/has-data_1773852149000.png" alt="HasData logo" width="28" height="28"> HasData: Universal API

Extract, monitor, and enrich web data across search and marketplace sites

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hasData/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hasdata.com
- **Vendor API docs:** https://docs.hasdata.com/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Scrape Job](actions/get-batch-scrape-job.md) | GET | Retrieves a batch scrape job from HasData. |
| [Submit Batch Scrape Job](actions/submit-batch-scrape-job.md) | GET | Submits a batch web scrape job to HasData. |

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [List Batch Scrape Results](actions/list-batch-scrape-results.md) | GET | Retrieves results for a HasData batch scrape job. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Shopify Collections](actions/list-shopify-collections.md) | GET | Retrieves Shopify collections from HasData. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Events](actions/search-google-events.md) | GET | Retrieves Google Events results from HasData. |

### Flight

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Flights](actions/search-google-flights.md) | GET | Retrieves Google Flights results from HasData. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Images](actions/search-google-images.md) | GET | Retrieves Google Images results from HasData. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Indeed Job](actions/get-indeed-job.md) | GET | Retrieves an Indeed job from HasData. |

### Job Listing

| Action | Method | Description |
| --- | --- | --- |
| [Search Indeed Listings](actions/search-indeed-listings.md) | GET | Retrieves Indeed listings from HasData. |

### Listing

| Action | Method | Description |
| --- | --- | --- |
| [Search Airbnb Listings](actions/search-airbnb-listings.md) | GET | Retrieves Airbnb listings from HasData. |
| [Search Redfin Listings](actions/search-redfin-listings.md) | GET | Retrieves Redfin listings from HasData. |
| [Search Zillow Listings](actions/search-zillow-listings.md) | GET | Retrieves Zillow listings from HasData. |

### News Item

| Action | Method | Description |
| --- | --- | --- |
| [Search Google News](actions/search-google-news.md) | GET | Retrieves Google News results from HasData. |

### Place

| Action | Method | Description |
| --- | --- | --- |
| [Get Yelp Place](actions/get-yelp-place.md) | GET | Retrieves a Yelp place from HasData. |
| [Search Google Maps](actions/search-google-maps.md) | GET | Retrieves Google Maps search results from HasData. |
| [Search Yelp Places](actions/search-yelp-places.md) | GET | Retrieves Yelp place results from HasData. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Shopify Products](actions/list-shopify-products.md) | GET | Retrieves Shopify products from HasData. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Airbnb Property](actions/get-airbnb-property.md) | GET | Retrieves an Airbnb property from HasData. |
| [Get Redfin Property](actions/get-redfin-property.md) | GET | Retrieves a Redfin property from HasData. |
| [Get Zillow Property](actions/get-zillow-property.md) | GET | Retrieves a Zillow property from HasData. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Google Maps Reviews](actions/list-google-maps-reviews.md) | GET | Retrieves Google Maps reviews from HasData. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google SERP](actions/search-google-serp.md) | GET | Retrieves Google SERP results from HasData. |
| [Search Google SERP Light](actions/search-google-serp-light.md) | GET | Retrieves Google SERP Light results from HasData. |

### Trend

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Trends](actions/search-google-trends.md) | GET | Retrieves Google Trends results from HasData. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves HasData usage and concurrency details. |

### Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Web Page](actions/scrape-web-page.md) | GET | Retrieves scraped web page data from HasData. |

