# List Item Aspects for Category with eBay

Returns a complete list of aspects for all of the leaf categories that belong to an eBay marketplace.

## Endpoint

- **Method:** `GET`
- **Path:** `commerce/taxonomy/v1/category_tree/0/get_item_aspects_for_category`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [List Item Aspects for Category](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getItemAspectsForCategory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | query | `string` | yes | The unique identifier of the leaf category for which aspects are being requested. |
