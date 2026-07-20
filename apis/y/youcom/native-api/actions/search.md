# Search with You.com

Retrieves search results from You.com.

## Endpoint

- **Method:** `GET`
- **Path:** `https://ydc-index.io/v1/search`
- **Base URL:** `https://api.you.com`
- **Official documentation:** [Search](https://docs.you.com/api-reference/search/v1-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query. |
| `count` | query | `number` | no | Maximum results per section. |
| `freshness` | query | `string` | no | Filter results by recency. |
| `country` | query | `string` | no | Country code target. |
| `language` | query | `string` | no | BCP 47 language code. |
| `safesearch` | query | `string` | no | Safety level. |
| `livecrawl` | query | `string` | no | Include full page content. |
| `livecrawl_formats` | query | `string` | no | Formats for livecrawl output. |
| `crawl_timeout` | query | `number` | no | Livecrawl timeout in seconds. |
| `offset` | query | `number` | no | Pagination offset. |
