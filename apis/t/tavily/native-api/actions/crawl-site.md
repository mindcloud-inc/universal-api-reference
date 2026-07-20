# Crawl Site with Tavily

Crawls a website from a base URL with Tavily.

## Endpoint

- **Method:** `POST`
- **Path:** `/crawl`
- **Base URL:** `https://api.tavily.com`
- **Official documentation:** [Crawl Site](https://docs.tavily.com/documentation/api-reference/endpoint/crawl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_external` | body | `boolean` | no | Whether to include external domain links in the results. |
| `chunks_per_source` | body | `number` | no | Maximum number of relevant chunks to return per source when instructions are provided. |
| `exclude_domains[]` | body | `array<string>` | no | Regex patterns to exclude specific domains or subdomains. |
| `exclude_paths[]` | body | `array<string>` | no | Regex patterns to exclude specific URL paths. |
| `extract_depth` | body | `string` | no | Extraction depth. Accepted values are basic or advanced. |
| `format` | body | `string` | no | Content format. Accepted values are markdown or text. |
| `include_favicon` | body | `boolean` | no | Whether to include the favicon URL for each result. |
| `include_images` | body | `boolean` | no | Whether to include images in the crawl results. |
| `include_usage` | body | `boolean` | no | Include credit usage information in the response. |
| `instructions` | body | `string` | no | Natural language instructions for the crawler. |
| `limit` | body | `number` | no | Total number of links the crawler will process before stopping. |
| `max_breadth` | body | `number` | no | Max number of links to follow per page. |
| `max_depth` | body | `number` | no | Max depth of the crawl from the root URL. |
| `select_domains[]` | body | `array<string>` | no | Regex patterns to include only specific domains or subdomains. |
| `select_paths[]` | body | `array<string>` | no | Regex patterns to include only specific URL paths. |
| `timeout` | body | `number` | no | Maximum time in seconds to wait for the crawl operation before timing out. |
| `url` | body | `string` | yes | The root URL to begin the crawl. |
