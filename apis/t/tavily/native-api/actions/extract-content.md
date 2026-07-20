# Extract Content with Tavily

Retrieves web page content from URLs with Tavily.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.tavily.com`
- **Official documentation:** [Extract Content](https://docs.tavily.com/documentation/api-reference/endpoint/extract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chunks_per_source` | body | `number` | no | Maximum number of relevant chunks to return per source when query is provided. |
| `extract_depth` | body | `string` | no | Extraction depth. Accepted values are basic or advanced. |
| `format` | body | `string` | no | Content format. Accepted values are markdown or text. |
| `include_favicon` | body | `boolean` | no | Include the favicon URL for each result. |
| `include_images` | body | `boolean` | no | Include extracted images in the response. |
| `include_usage` | body | `boolean` | no | Include credit usage information in the response. |
| `query` | body | `string` | no | Optional user intent used to rerank extracted content chunks. |
| `timeout` | body | `number` | no | Maximum time in seconds to wait before timing out the extraction. |
| `urls[]` | body | `array<string>` | yes | One or more URLs to extract content from. |
