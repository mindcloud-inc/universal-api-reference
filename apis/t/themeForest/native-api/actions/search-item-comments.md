# Search Item Comments with Themeforest

Finds comments for an Envato item by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/discovery/search/search/comment`
- **Base URL:** `https://api.envato.com`
- **Official documentation:** [Search Item Comments](https://build.envato.com/api/#search_getSearchComment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | query | `number` | yes | Envato item ID whose comments should be searched. |
| `sort_by` | query | `string` | no | Comment sort order: relevance, newest, or oldest. |
| `term` | query | `string` | no | Text to search for in item comments. |
| `page` | query | `number` | no | Result page number. |
| `page_size` | query | `number` | no | Number of comments per page. |
