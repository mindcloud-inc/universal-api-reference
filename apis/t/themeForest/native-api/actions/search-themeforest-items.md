# Search ThemeForest Items with Themeforest

Finds ThemeForest items by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/discovery/search/search/item`
- **Base URL:** `https://api.envato.com`
- **Official documentation:** [Search ThemeForest Items](https://build.envato.com/api/#search_getSearchItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | ThemeForest category filter. |
| `sort_by` | query | `string` | no | Sort field supported by Envato discovery search. |
| `sort_direction` | query | `string` | no | Sort direction supported by Envato discovery search. |
| `term` | query | `string` | no | Search text for matching ThemeForest items. |
| `page` | query | `number` | no | Result page number. |
| `page_size` | query | `number` | no | Number of results per page. |
