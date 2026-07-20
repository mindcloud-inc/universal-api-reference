# WebScraper.IO: Native API Reference

A consolidated summary of WebScraper.IO's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://webscraper.io/documentation/web-scraper-cloud/api
- **API base URL:** `https://api.webscraper.io/api/v1`

## Authentication

### API Token

Use your Web Scraper Cloud API token. MindCloud stores one token and sends it as the shared api_token query parameter on every request.

### Credentials

- **API Token:** `apiKey` · required · Your Web Scraper Cloud API token from the Web Scraper Cloud API page.

[Official authentication documentation](https://webscraper.io/documentation/web-scraper-cloud/api)

## API conventions

Response data is read from `data`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Scraping Job](actions/create-scraping-job.md) | `POST /scraping-job` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Create Sitemap](actions/create-sitemap.md) | `POST /sitemap` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Delete Scraping Job](actions/delete-scraping-job.md) | `DELETE /scraping-job/:scrapingJobId` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Delete Sitemap](actions/delete-sitemap.md) | `DELETE /sitemap/:sitemapId` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Disable Sitemap Scheduler](actions/disable-sitemap-scheduler.md) | `POST /sitemap/:sitemapId/disable-scheduler` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Download Scraping Job CSV](actions/download-scraping-job-csv.md) | `GET /scraping-job/:scrapingJobId/csv` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Download Scraping Job JSON](actions/download-scraping-job-json.md) | `GET /scraping-job/:scrapingJobId/json` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Download Scraping Job XLSX](actions/download-scraping-job-xlsx.md) | `GET /scraping-job/:scrapingJobId/xlsx` | [docs](https://github.com/webscraperio/api-client-php/blob/master/src/ApiClient/Client.php) |
| [Enable Sitemap Scheduler](actions/enable-sitemap-scheduler.md) | `POST /sitemap/:sitemapId/enable-scheduler` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Get Account Info](actions/get-account-info.md) | `GET /account` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Get Scraping Job](actions/get-scraping-job.md) | `GET /scraping-job/:scrapingJobId` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Get Scraping Job Data Quality](actions/get-scraping-job-data-quality.md) | `GET /scraping-job/:scrapingJobId/data-quality` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Get Scraping Job Problematic URLs](actions/get-scraping-job-problematic-urls.md) | `GET /scraping-job/:scrapingJobId/problematic-urls` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Get Sitemap](actions/get-sitemap.md) | `GET /sitemap/:sitemapId` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Get Sitemap Scheduler](actions/get-sitemap-scheduler.md) | `GET /sitemap/:sitemapId/scheduler` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [List Scraping Jobs](actions/list-scraping-jobs.md) | `GET /scraping-jobs` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [List Sitemaps](actions/list-sitemaps.md) | `GET /sitemaps` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
| [Update Sitemap](actions/update-sitemap.md) | `PUT /sitemap/:sitemapId` | [docs](https://webscraper.io/documentation/web-scraper-cloud/api) |
