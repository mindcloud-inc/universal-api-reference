# Enable Sitemap Scheduler with WebScraper.IO

Enables scheduler settings for a sitemap in WebScraper.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/sitemap/:sitemapId/enable-scheduler`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Enable Sitemap Scheduler](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cron_day` | body | `string` | yes | Cron day-of-month expression. |
| `cron_hour` | body | `string` | yes | Cron hour expression. |
| `cron_minute` | body | `string` | yes | Cron minute expression. |
| `cron_month` | body | `string` | yes | Cron month expression. |
| `cron_timezone` | body | `string` | yes | Timezone for the cron schedule. |
| `cron_weekday` | body | `string` | yes | Cron weekday expression. |
| `driver` | body | `string` | yes | Scraping driver: fast or fulljs. |
| `page_load_delay` | body | `number` | yes | Delay after page load in milliseconds. |
| `proxy` | body | `string` | yes | Proxy region code. |
| `request_interval` | body | `number` | yes | Delay between requests in milliseconds. |
| `sitemapId` | path | `number` | yes | The Web Scraper sitemap ID. |
