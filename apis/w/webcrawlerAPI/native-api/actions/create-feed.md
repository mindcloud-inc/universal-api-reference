# Create Feed with Webcrawler API

Creates a scheduled website monitoring feed in Webcrawler API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/feed`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Create Feed](https://webcrawlerapi.com/docs/api/feed/feed-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to monitor. |
| `name` | body | `string` | no | Friendly feed name. |
| `scrape_type` | body | `string` | no | Content format for feed items. |
| `items_limit` | body | `number` | no | Maximum pages per crawl run. |
| `respect_robots_txt` | body | `boolean` | no | Whether to honor robots.txt. |
| `max_depth` | body | `number` | no | Maximum crawl depth. |
| `allow_subdomains` | body | `boolean` | no | Whether the feed may crawl subdomains. |
| `main_content_only` | body | `boolean` | no | Whether extraction should focus on main content only. |
| `whitelist_regexp` | body | `string` | no | Only include URLs matching this regular expression. |
| `blacklist_regexp` | body | `string` | no | Exclude URLs matching this regular expression. |
| `webhook_url` | body | `string` | no | Webhook URL for feed run notifications. |
