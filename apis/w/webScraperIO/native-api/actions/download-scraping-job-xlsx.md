# Download Scraping Job XLSX with WebScraper.IO

Downloads scraping job data as XLSX from WebScraper.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraping-job/:scrapingJobId/xlsx`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Download Scraping Job XLSX](https://github.com/webscraperio/api-client-php/blob/master/src/ApiClient/Client.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrapingJobId` | path | `number` | yes | Scraping job identifier. |
| `raw` | query | `boolean` | no | Return raw exported data when true. |
