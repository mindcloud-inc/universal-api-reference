# Search Web with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/tools/web-search`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Search Web](https://langbase.com/docs/api-reference/tools/web-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webSearchKey` | body | `string` | yes | Langbase web search key for the `LB-WEB-SEARCH-KEY` request header. |
| `query` | body | `string` | yes | Search query to run. |
| `service` | body | `list` | yes | Web search provider service. Accepted values: `0`. |
| `totalResults` | body | `number` | no | Maximum number of search results to return. |
