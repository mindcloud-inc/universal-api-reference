# Start Crawl with Firecrawl

Creates a crawl job in Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/crawl`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Start Crawl](https://docs.firecrawl.dev/api-reference/endpoint/crawl-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The base URL to start crawling from |
| `prompt` | body | `string` | no | Prompt to generate crawler options from natural language |
| `excludePaths[]` | body | `array<string>` | no | URL pathname regex patterns to exclude from the crawl |
| `includePaths[]` | body | `array<string>` | no | URL pathname regex patterns to include in the crawl |
| `maxDiscoveryDepth` | body | `number` | no | Maximum discovery depth to crawl |
| `sitemap` | body | `string` | no | Sitemap mode when crawling |
| `ignoreQueryParameters` | body | `boolean` | no | Do not re-scrape the same path with different query parameters |
| `regexOnFullURL` | body | `boolean` | no | Match include and exclude regexes against the full URL |
| `limit` | body | `number` | no | Maximum number of pages to crawl |
| `crawlEntireDomain` | body | `boolean` | no | Allow crawling internal sibling and parent URLs |
| `allowExternalLinks` | body | `boolean` | no | Allow the crawler to follow external links |
| `allowSubdomains` | body | `boolean` | no | Allow the crawler to follow subdomain links |
| `delay` | body | `number` | no | Delay in seconds between scrapes |
| `maxConcurrency` | body | `number` | no | Maximum number of concurrent scrapes |
| `webhook` | body | `object` | no | Webhook specification for crawl events |
| `scrapeOptions` | body | `object` | no | Scrape options to apply to each crawled page |
| `zeroDataRetention` | body | `boolean` | no | Enable zero data retention for this crawl |
