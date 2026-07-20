# Search Web with Firecrawl

Finds web results with Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Search Web](https://docs.firecrawl.dev/api-reference/endpoint/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The search query |
| `limit` | body | `number` | no | Maximum number of results to return |
| `sources[]` | body | `array<object>` | no | Sources to search |
| `categories[]` | body | `array<object>` | no | Categories to filter results by |
| `tbs` | body | `string` | no | Time-based search parameter |
| `location` | body | `string` | no | Location parameter for search results |
| `country` | body | `string` | no | ISO country code for geo-targeting search results |
| `timeout` | body | `number` | no | Timeout in milliseconds |
| `ignoreInvalidURLs` | body | `boolean` | no | Exclude URLs that are invalid for other Firecrawl endpoints |
| `scrapeOptions` | body | `object` | no | Options for scraping search results |
