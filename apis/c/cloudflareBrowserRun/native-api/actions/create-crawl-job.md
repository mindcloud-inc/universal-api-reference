# Create Crawl Job with Cloudflare Browser Run

Creates a crawl job in Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/crawl`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Create Crawl Job](https://developers.cloudflare.com/browser-rendering/rest-api/crawl-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Starting URL for the crawl job. |
| `formats[]` | body | `array<string>` | no | Formats to return from the crawl: html, markdown, or json. |
| `depth` | body | `number` | no | Maximum number of levels deep the crawler will traverse from the starting URL. |
| `limit` | body | `number` | no | Maximum number of URLs to crawl. |
| `render` | body | `boolean` | no | Whether to render pages or fetch static content. True by default. |
| `options` | body | `object` | no | Crawler options for include/exclude patterns, subdomains, and external links. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
