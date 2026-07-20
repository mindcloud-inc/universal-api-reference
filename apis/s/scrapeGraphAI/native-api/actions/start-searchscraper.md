# Start SearchScraper with ScrapeGraphAI

Starts a SearchScraper search job in ScrapeGraphAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/searchscraper`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Start SearchScraper](https://docs.scrapegraphai.com/api-reference/endpoint/searchscraper/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headers` | body | `object` | no | Optional custom headers for the search request. |
| `mock` | body | `boolean` | no | Return mock data instead of performing a live search. |
| `output_schema` | body | `object` | no | Optional schema object to structure search results. |
| `stealth` | body | `boolean` | no | Enable stealth mode to bypass bot protection. |
| `time_range` | body | `string` | no | Filter results by recency. |
| `user_prompt` | body | `string` | yes | Search query or question to answer. |
