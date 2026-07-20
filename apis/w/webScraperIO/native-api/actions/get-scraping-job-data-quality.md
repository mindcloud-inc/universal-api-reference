# Get Scraping Job Data Quality with WebScraper.IO

Retrieves data quality statistics for a WebScraper.IO scraping job.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraping-job/:scrapingJobId/data-quality`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Get Scraping Job Data Quality](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrapingJobId` | path | `number` | yes | The Web Scraper scraping job ID. |
