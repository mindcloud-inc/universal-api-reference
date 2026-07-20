# Map Website with Firecrawl

Retrieves website URLs from Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/map`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Map Website](https://docs.firecrawl.dev/api-reference/endpoint/map)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The base URL to start crawling from |
| `search` | body | `string` | no | Specify a search query to order the results by relevance |
| `sitemap` | body | `string` | no | Sitemap mode when mapping |
| `includeSubdomains` | body | `boolean` | no | Include subdomains of the website |
| `ignoreQueryParameters` | body | `boolean` | no | Do not return URLs with query parameters |
| `ignoreCache` | body | `boolean` | no | Bypass the sitemap cache to retrieve fresh URLs |
| `limit` | body | `number` | no | Maximum number of links to return |
| `timeout` | body | `number` | no | Timeout in milliseconds |
| `location` | body | `object` | no | Location settings for the request |
