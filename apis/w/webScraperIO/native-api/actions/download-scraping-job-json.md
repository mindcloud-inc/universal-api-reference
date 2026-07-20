# Download Scraping Job JSON with WebScraper.IO

Downloads scraping job data as JSONL from WebScraper.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraping-job/:scrapingJobId/json`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Download Scraping Job JSON](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrapingJobId` | path | `number` | yes | The Web Scraper scraping job ID. |
| `raw` | query | `boolean` | no | Return raw exported data when true. |
