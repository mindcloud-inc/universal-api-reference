# Find Similar Items with Themeforest

Finds items similar to an Envato item.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/discovery/search/search/more_like_this`
- **Base URL:** `https://api.envato.com`
- **Official documentation:** [Find Similar Items](https://build.envato.com/api/#search_getSearchMoreLikeThis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | query | `number` | yes | Envato item ID to use as the similarity seed. |
| `page` | query | `number` | no | Result page number. |
| `page_size` | query | `number` | no | Number of similar items per page. |
