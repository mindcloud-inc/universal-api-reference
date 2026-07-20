# Search Regulations with eCFR

Searches regulations in eCFR by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search/v1/results`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Search Regulations](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text, such as agriculture. |
| `order` | query | `list` | no | Optional result ordering: relevance, citations, hierarchy, newest_first, oldest_first, or suggestions. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `per_page` | query | `number` | no | Maximum number of search results to return per page. |
| `page` | query | `number` | no | One-based search results page number. |
