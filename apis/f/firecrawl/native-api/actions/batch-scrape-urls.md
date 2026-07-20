# Batch Scrape URLs with Firecrawl

Creates a batch scrape job in Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch/scrape`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Batch Scrape URLs](https://docs.firecrawl.dev/api-reference/endpoint/batch-scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | The URLs to scrape |
| `formats[]` | body | `array<string>` | no | Output formats to return for each scraped URL |
| `onlyMainContent` | body | `boolean` | no | Return only the main content of each page |
| `includeTags[]` | body | `array<string>` | no | HTML tags to include in the output |
| `excludeTags[]` | body | `array<string>` | no | HTML tags to exclude from the output |
| `maxAge` | body | `number` | no | Maximum cache age in milliseconds |
| `minAge` | body | `number` | no | Minimum cache age in milliseconds for cache-only reads |
| `headers` | body | `object` | no | Custom request headers for the target sites |
| `waitFor` | body | `number` | no | Delay before scraping in milliseconds |
| `mobile` | body | `boolean` | no | Emulate a mobile device |
| `skipTlsVerification` | body | `boolean` | no | Skip TLS certificate verification when making requests |
| `timeout` | body | `number` | no | Request timeout in milliseconds |
| `parsers[]` | body | `array<object>` | no | File parsing controls for supported file types |
| `actions[]` | body | `array<object>` | no | Browser actions to run before scraping each page |
| `location` | body | `object` | no | Geo and language settings for the request |
| `removeBase64Images` | body | `boolean` | no | Replace embedded base64 images in markdown output |
| `blockAds` | body | `boolean` | no | Enable ad and cookie popup blocking |
| `proxy` | body | `string` | no | Proxy mode to use for scraping |
| `storeInCache` | body | `boolean` | no | Store the scraped pages in Firecrawl cache and index |
| `webhook` | body | `object` | no | Webhook specification for batch scrape events |
| `maxConcurrency` | body | `number` | no | Maximum number of concurrent scrapes |
| `ignoreInvalidURLs` | body | `boolean` | no | Ignore invalid URLs instead of failing the entire request |
| `zeroDataRetention` | body | `boolean` | no | Enable zero data retention for this batch scrape |
