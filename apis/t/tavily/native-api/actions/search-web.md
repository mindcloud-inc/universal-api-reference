# Search Web with Tavily

Finds web search results in Tavily by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.tavily.com`
- **Official documentation:** [Search Web](https://docs.tavily.com/documentation/api-reference/endpoint/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chunks_per_source` | body | `number` | no | The maximum number of relevant content chunks to return per source when search depth is advanced. |
| `country` | body | `string` | no | Prioritize search results from a specific country when topic is general. |
| `end_date` | body | `date` | no | Return results before this date in YYYY-MM-DD format. |
| `exclude_domains[]` | body | `array<string>` | no | A list of domains to specifically exclude from the search results. |
| `include_answer` | body | `string` | no | Include an LLM-generated answer. Accepted values are false, true, basic, or advanced. |
| `include_domains[]` | body | `array<string>` | no | A list of domains to specifically include in the search results. |
| `include_image_descriptions` | body | `boolean` | no | When include images is true, also return a description for each image. |
| `include_raw_content` | body | `string` | no | Include cleaned HTML content from each result. Accepted values are false, true, markdown, or text. |
| `query` | body | `string` | yes | The search query to execute with Tavily. |
| `start_date` | body | `date` | no | Return results after this date in YYYY-MM-DD format. |
| `time_range` | body | `string` | no | The time range back from the current date to filter results by publish or update date. |
| `timeout` | body | `number` | no | Maximum time in seconds to wait for the search request. |
| `search_depth` | body | `string` | no | Controls the latency versus relevance tradeoff for the search. |
| `topic` | body | `string` | no | The category of the search. |
| `max_results` | body | `number` | no | The maximum number of search results to return. |
| `include_images` | body | `boolean` | no | Also perform an image search and include image results. |
| `include_favicon` | body | `boolean` | no | Include favicon URLs for each result when available. |
| `auto_parameters` | body | `boolean` | no | Automatically configure search parameters based on the query intent. |
| `exact_match` | body | `boolean` | no | Return only results containing the quoted exact phrase. |
| `include_usage` | body | `boolean` | no | Include credit usage information in the response. |
