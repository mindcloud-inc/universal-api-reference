# Create Scrape Job with Webcrawler API

Creates a single-page scrape job in Webcrawler API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/scrape`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Create Scrape Job](https://webcrawlerapi.com/docs/api/scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Target page URL to scrape. |
| `include_links` | query | `boolean` | no | Include discovered links in the scrape result. |
| `output_format` | body | `string` | no | Requested scrape output format. |
| `prompt` | body | `string` | no | Optional extraction prompt for the scrape. |
| `clean_selectors` | body | `string` | no | Selectors to remove before returning cleaned content. |
| `main_content_only` | body | `boolean` | no | Whether to focus extraction on the page's main content. |
| `respect_robots_txt` | body | `boolean` | no | Whether to respect robots.txt rules. |
