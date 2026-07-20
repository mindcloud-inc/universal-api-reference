# Get Contents with Exa

Retrieves page contents from Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/contents`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Get Contents](https://exa.ai/docs/reference/get-contents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | Array of URLs to crawl (backwards compatible with 'ids' parameter). |
| `ids[]` | body | `array<string>` | no | Deprecated - use 'urls' instead. Array of document IDs obtained from searches. |
| `text.maxCharacters` | body | `number` | no | Maximum character limit for the full page text. Useful for controlling response size and API costs. |
| `text.includeHtmlTags` | body | `boolean` | no | Include HTML tags in the response, which can help LLMs understand text structure and formatting. |
| `highlights.numSentences` | body | `number` | no | The number of sentences to return for each snippet. |
| `highlights.highlightsPerUrl` | body | `number` | no | The number of snippets to return for each result. |
| `highlights.query` | body | `string` | no | Custom query to direct the LLM's selection of highlights. |
| `summary` | body | `object` | no | Summary of the webpage |
| `livecrawl` | body | `string` | no | Options for livecrawling pages. 'never': Disable livecrawling (default for neural search). 'fallback': Livecrawl when cache is empty. 'always': Always livecrawl. 'preferred': Always try to livecrawl, but fall back to cache if crawling fails. |
| `livecrawlTimeout` | body | `number` | no | The timeout for livecrawling in milliseconds. |
| `maxAgeHours` | body | `number` | no | Maximum age of cached content in hours. Controls when livecrawling is triggered based on content freshness. - Positive value (e.g. 24): Use cached content if it's less than this many hours old, otherwise livecrawl. - 0: Always livecrawl, never use cache. - -1: Never livecrawl, always use cache. - Omit (default): Livecrawl as fallback only when no cached content exists. |
| `subpages` | body | `number` | no | The number of subpages to crawl. The actual number crawled may be limited by system constraints. |
| `subpageTarget` | body | `string` | no | — |
| `extras.links` | body | `number` | no | Number of URLs to return from each webpage. |
| `extras.imageLinks` | body | `number` | no | Number of images to return for each result. |
| `context.maxCharacters` | body | `number` | no | Maximum character limit. |
