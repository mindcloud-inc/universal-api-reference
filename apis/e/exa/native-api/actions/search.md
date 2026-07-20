# Search with Exa

Finds relevant search results in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Search](https://exa.ai/docs/reference/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The query string for the search. |
| `additionalQueries[]` | body | `array<string>` | no | Additional query variations for deep search. Only works with type="deep". When provided, these queries are used alongside the main query for comprehensive results. |
| `type` | body | `string` | no | The type of search. Neural uses an embeddings-based model, auto (default) intelligently combines available search methods, fast uses streamlined versions of the neural model, and deep provides comprehensive search with query expansion and detailed context. |
| `category` | body | `string` | no | A data category to focus on. |
| `userLocation` | body | `string` | no | The two-letter ISO country code of the user, e.g. US. |
| `numResults` | body | `number` | no | Number of results to return (up to thousands of results available for custom plans) |
| `includeDomains[]` | body | `array<string>` | no | List of domains to include in the search. If specified, results will only come from these domains. |
| `excludeDomains[]` | body | `array<string>` | no | List of domains to exclude from search results. If specified, no results will be returned from these domains. |
| `startCrawlDate` | body | `date` | no | Crawl date refers to the date that Exa discovered a link. Results will include links that were crawled after this date. Must be specified in ISO 8601 format. |
| `endCrawlDate` | body | `date` | no | Crawl date refers to the date that Exa discovered a link. Results will include links that were crawled before this date. Must be specified in ISO 8601 format. |
| `startPublishedDate` | body | `date` | no | Only links with a published date after this will be returned. Must be specified in ISO 8601 format. |
| `endPublishedDate` | body | `date` | no | Only links with a published date before this will be returned. Must be specified in ISO 8601 format. |
| `includeText[]` | body | `array<string>` | no | List of strings that must be present in webpage text of results. Currently, only 1 string is supported, of up to 5 words. |
| `excludeText[]` | body | `array<string>` | no | List of strings that must not be present in webpage text of results. Currently, only 1 string is supported, of up to 5 words. Checks from the first 1000 words of the webpage text. |
| `context.maxCharacters` | body | `number` | no | Maximum character limit. |
| `contents` | body | `object` | no | — |
