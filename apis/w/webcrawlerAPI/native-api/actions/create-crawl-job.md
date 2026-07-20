# Create Crawl Job with Webcrawler API

Creates a website crawl job in Webcrawler API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/crawl`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Create Crawl Job](https://webcrawlerapi.com/docs/api/crawl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Target website URL to crawl. |
| `scrape_type` | body | `string` | no | Output format for crawled content. |
| `items_limit` | body | `number` | no | Maximum number of items to return. |
| `max_depth` | body | `number` | no | Maximum crawl depth. |
| `respect_robots_txt` | body | `boolean` | no | Whether to respect robots.txt rules. |
| `allow_subdomains` | body | `boolean` | no | Whether to crawl subdomains. |
| `main_content_only` | body | `boolean` | no | Whether to limit extraction to main content. |
| `whitelist_regexp` | body | `string` | no | Only include URLs matching this regular expression. |
| `blacklist_regexp` | body | `string` | no | Exclude URLs matching this regular expression. |
| `webhook_url` | body | `string` | no | Webhook URL for job completion notifications. |
