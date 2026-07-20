# Download Scraping Job CSV with WebScraper.IO

Downloads scraping job data as CSV from WebScraper.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraping-job/:scrapingJobId/csv`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Download Scraping Job CSV](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrapingJobId` | path | `number` | yes | The Web Scraper scraping job ID. |
| `raw` | query | `boolean` | no | Return raw exported data when true. |
