# List Items with Walmart

Retrieve all items from a partner’s catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/items`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST (nextCursor)
- **Official documentation:** [List Items](https://developer.walmart.com/us-marketplace/reference/getallitems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lifecycleStatus` | query | `list<string>` | no | The status of an item in the overall lifecycle. |
| `publishedStatus` | query | `list<string>` | no | The status of an item in the submission process. |
| `condition` | query | `list<string>` | no | The condition of a product. |
| `availability` | query | `list<string>` | no | The availability of a product. |
| `showDuplicateItemInfo` | query | `boolean` | no | Indicates whether to include details of duplicate items in the response. Set this parameter to true if you want to receive information on duplicate items. Format: `toggle`. |
| `includeCustomerFavoritesStatus` | query | `boolean` | no | Toggle on to include isCustomerFavorite item details in the response. Format: `toggle`. |
