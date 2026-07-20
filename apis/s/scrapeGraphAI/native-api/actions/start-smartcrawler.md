# Start SmartCrawler with ScrapeGraphAI

Starts a SmartCrawler crawl job in ScrapeGraphAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/crawl`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Start SmartCrawler](https://docs.scrapegraphai.com/api-reference/endpoint/smartcrawler/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_size` | body | `number` | no | Number of pages to process in each batch. |
| `breadth` | body | `number` | no | Maximum number of links to crawl per depth level. |
| `cache_website` | body | `boolean` | no | Whether to cache website content. |
| `depth` | body | `number` | no | Maximum crawl depth. |
| `extraction_mode` | body | `boolean` | no | When false, use markdown conversion mode instead of AI extraction. |
| `max_pages` | body | `number` | no | Maximum number of pages to crawl. |
| `prompt` | body | `string` | no | Extraction instructions, required when Extraction Mode is true. |
| `rules` | body | `object` | no | Optional crawl rules object for include and exclude logic. |
| `same_domain_only` | body | `boolean` | no | Restrict crawling to the same domain. |
| `schema` | body | `object` | no | Optional JSON schema object for structured extraction output. |
| `sitemap` | body | `boolean` | no | Use sitemap.xml for discovery. |
| `stealth` | body | `boolean` | no | Enable stealth mode to bypass bot protection. |
| `url` | body | `string` | yes | Starting URL for the crawl. |
| `wait_ms` | body | `number` | no | Milliseconds to wait before scraping each page. |
| `webhook_url` | body | `string` | no | Webhook URL to receive completion notifications. |
