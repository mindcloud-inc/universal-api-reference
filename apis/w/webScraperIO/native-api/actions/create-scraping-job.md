# Create Scraping Job with WebScraper.IO

Creates a new scraping job in WebScraper.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/scraping-job`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Create Scraping Job](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_id` | body | `string` | no | Optional custom identifier included in notifications. |
| `driver` | body | `string` | yes | Scraping driver: fast or fulljs. |
| `page_load_delay` | body | `number` | yes | Delay after page load in milliseconds. |
| `proxy` | body | `string` | yes | Proxy region code. |
| `request_interval` | body | `number` | yes | Delay between requests in milliseconds. |
| `sitemap_id` | body | `number` | yes | The sitemap to scrape. |
| `start_urls[]` | body | `array<string>` | no | Optional start URLs override for the job. |
