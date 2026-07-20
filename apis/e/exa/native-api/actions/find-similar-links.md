# Find Similar Links with Exa

Finds links similar to a URL in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/findSimilar`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Find Similar Links](https://exa.ai/docs/reference/find-similar-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The url for which you would like to find similar links. |
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
