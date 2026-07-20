# HasData: Native API Reference

A consolidated summary of HasData's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.hasdata.com/introduction
- **API base URL:** `https://api.hasdata.com`

## Authentication

### API Key

Use your HasData API key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.hasdata.com/apis/web-scraping-api/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Airbnb Property](actions/get-airbnb-property.md) | `GET /scrape/airbnb/property` | [docs](https://docs.hasdata.com/apis/airbnb/property) |
| [Get Batch Scrape Job](actions/get-batch-scrape-job.md) | `GET /scrape/batch/web/:jobId` | [docs](https://docs.hasdata.com/apis/web-scraping-api/batch-scrape) |
| [Get Indeed Job](actions/get-indeed-job.md) | `GET /scrape/indeed/job` | [docs](https://docs.hasdata.com/apis/indeed/job) |
| [Get Redfin Property](actions/get-redfin-property.md) | `GET /scrape/redfin/property` | [docs](https://docs.hasdata.com/apis/redfin/property) |
| [Get Usage](actions/get-usage.md) | `GET /user/me/usage` | [docs](https://docs.hasdata.com/credits-and-concurrency) |
| [Get Yelp Place](actions/get-yelp-place.md) | `GET /scrape/yelp/place` | [docs](https://docs.hasdata.com/apis/yelp/place) |
| [Get Zillow Property](actions/get-zillow-property.md) | `GET /scrape/zillow/property` | [docs](https://docs.hasdata.com/apis/zillow/property) |
| [List Batch Scrape Results](actions/list-batch-scrape-results.md) | `GET /scrape/batch/web/:jobId/results` | [docs](https://docs.hasdata.com/apis/web-scraping-api/batch-scrape) |
| [List Google Maps Reviews](actions/list-google-maps-reviews.md) | `GET /scrape/google-maps/reviews` | [docs](https://docs.hasdata.com/apis/google-maps/reviews) |
| [List Shopify Collections](actions/list-shopify-collections.md) | `GET /scrape/shopify/collections` | [docs](https://docs.hasdata.com/apis/shopify/collections) |
| [List Shopify Products](actions/list-shopify-products.md) | `GET /scrape/shopify/products` | [docs](https://docs.hasdata.com/apis/shopify/products) |
| [Scrape Web Page](actions/scrape-web-page.md) | `POST /scrape/web` | [docs](https://docs.hasdata.com/apis/web-scraping-api/quickstart) |
| [Search Airbnb Listings](actions/search-airbnb-listings.md) | `GET /scrape/airbnb/listing` | [docs](https://docs.hasdata.com/apis/airbnb/listing) |
| [Search Google Events](actions/search-google-events.md) | `GET /scrape/google/events` | [docs](https://docs.hasdata.com/apis/google-serp/events) |
| [Search Google Flights](actions/search-google-flights.md) | `GET /scrape/google/flights` | [docs](https://docs.hasdata.com/apis/google-travel/flights) |
| [Search Google Images](actions/search-google-images.md) | `GET /scrape/google/images` | [docs](https://docs.hasdata.com/apis/google-images/images) |
| [Search Google Maps](actions/search-google-maps.md) | `GET /scrape/google-maps/search` | [docs](https://docs.hasdata.com/apis/google-maps/search) |
| [Search Google News](actions/search-google-news.md) | `GET /scrape/google/news` | [docs](https://docs.hasdata.com/apis/google-serp/news) |
| [Search Google SERP](actions/search-google-serp.md) | `GET /scrape/google/serp` | [docs](https://docs.hasdata.com/apis/google-serp-api/quickstart) |
| [Search Google SERP Light](actions/search-google-serp-light.md) | `GET /scrape/google-light/serp` | [docs](https://docs.hasdata.com/apis/google-serp/serp-light) |
| [Search Google Trends](actions/search-google-trends.md) | `GET /scrape/google-trends/search` | [docs](https://docs.hasdata.com/apis/google-trends/search) |
| [Search Indeed Listings](actions/search-indeed-listings.md) | `GET /scrape/indeed/listing` | [docs](https://docs.hasdata.com/apis/indeed/listing) |
| [Search Redfin Listings](actions/search-redfin-listings.md) | `GET /scrape/redfin/listing` | [docs](https://docs.hasdata.com/apis/redfin/listing) |
| [Search Yelp Places](actions/search-yelp-places.md) | `GET /scrape/yelp/search` | [docs](https://docs.hasdata.com/apis/yelp/search) |
| [Search Zillow Listings](actions/search-zillow-listings.md) | `GET /scrape/zillow/listing` | [docs](https://docs.hasdata.com/apis/zillow/listing) |
| [Submit Batch Scrape Job](actions/submit-batch-scrape-job.md) | `POST /scrape/batch/web` | [docs](https://docs.hasdata.com/apis/web-scraping-api/batch-scrape) |
