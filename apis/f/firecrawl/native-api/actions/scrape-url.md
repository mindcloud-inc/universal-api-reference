# Scrape URL with Firecrawl

Scrapes a single URL with Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Scrape URL](https://docs.firecrawl.dev/api-reference/endpoint/scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to scrape |
| `formats[]` | body | `array<string>` | no | Output formats to return |
| `onlyMainContent` | body | `boolean` | no | Return only the main page content |
| `includeTags[]` | body | `array<string>` | no | HTML tags to include in the output |
| `excludeTags[]` | body | `array<string>` | no | HTML tags to exclude from the output |
| `maxAge` | body | `number` | no | Maximum cache age in milliseconds |
| `headers` | body | `object` | no | Custom request headers for the target site |
| `waitFor` | body | `number` | no | Delay before scraping in milliseconds |
| `mobile` | body | `boolean` | no | Emulate a mobile device |
| `timeout` | body | `number` | no | Request timeout in milliseconds |
| `actions[]` | body | `array<object>` | no | Browser actions to run before scraping |
| `location` | body | `object` | no | Geo and language settings for the request |
| `removeBase64Images` | body | `boolean` | no | Replace embedded base64 images in markdown output |
| `blockAds` | body | `boolean` | no | Enable ad and cookie popup blocking |
| `proxy` | body | `string` | no | Proxy mode to use for scraping |
| `storeInCache` | body | `boolean` | no | Store the result in Firecrawl cache and index |
| `zeroDataRetention` | body | `boolean` | no | Enable zero data retention for this scrape |
