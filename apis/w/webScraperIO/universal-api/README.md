# <img src="https://images.mindcloud.co/apps/icons/webscraper-io-favicon_1775767242242.png" alt="WebScraper.IO logo" width="28" height="28"> WebScraper.IO: Universal API

Manage Web Scraper Cloud sitemaps, scraping jobs, schedulers, exports, data quality, and account info through the Web Scraper Cloud API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webScraperIO/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webscraper.io/
- **Vendor API docs:** https://webscraper.io/documentation/web-scraper-cloud/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Scraping Job](actions/create-scraping-job.md) | POST | Creates a new scraping job in WebScraper.IO. |
| [Create Sitemap](actions/create-sitemap.md) | POST | Creates a new sitemap in WebScraper.IO. |
| [Delete Scraping Job](actions/delete-scraping-job.md) | DELETE | Deletes an existing scraping job from WebScraper.IO. |
| [Delete Sitemap](actions/delete-sitemap.md) | DELETE | Deletes an existing sitemap from WebScraper.IO. |
| [Disable Sitemap Scheduler](actions/disable-sitemap-scheduler.md) | DELETE | Disables scheduler settings for a sitemap in WebScraper.IO. |
| [Download Scraping Job CSV](actions/download-scraping-job-csv.md) | GET | Downloads scraping job data as CSV from WebScraper.IO. |
| [Download Scraping Job JSON](actions/download-scraping-job-json.md) | GET | Downloads scraping job data as JSONL from WebScraper.IO. |
| [Download Scraping Job XLSX](actions/download-scraping-job-xlsx.md) | GET | Downloads scraping job data as XLSX from WebScraper.IO. |
| [Enable Sitemap Scheduler](actions/enable-sitemap-scheduler.md) | PUT | Enables scheduler settings for a sitemap in WebScraper.IO. |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your WebScraper.IO account details and credits. |
| [Get Scraping Job](actions/get-scraping-job.md) | GET | Retrieves a specific scraping job from WebScraper.IO. |
| [Get Scraping Job Data Quality](actions/get-scraping-job-data-quality.md) | GET | Retrieves data quality statistics for a WebScraper.IO scraping job. |
| [Get Scraping Job Problematic URLs](actions/get-scraping-job-problematic-urls.md) | GET | Retrieves problematic URLs for a scraping job from WebScraper.IO. |
| [Get Sitemap](actions/get-sitemap.md) | GET | Retrieves a specific sitemap from WebScraper.IO. |
| [Get Sitemap Scheduler](actions/get-sitemap-scheduler.md) | GET | Retrieves scheduler settings for a sitemap from WebScraper.IO. |
| [List Scraping Jobs](actions/list-scraping-jobs.md) | GET | Lists scraping jobs in your WebScraper.IO organization. |
| [List Sitemaps](actions/list-sitemaps.md) | GET | Lists sitemaps in your WebScraper.IO organization. |
| [Update Sitemap](actions/update-sitemap.md) | PUT | Updates an existing sitemap in WebScraper.IO. |

