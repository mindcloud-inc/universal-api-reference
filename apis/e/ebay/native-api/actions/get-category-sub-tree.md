# Get Category Sub-Tree with eBay

Retrieves a category Sub-Tree.

## Endpoint

- **Method:** `GET`
- **Path:** `commerce/taxonomy/v1/category_tree/:categoryTreeID/get_category_subtree`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Get Category Sub-Tree](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getCategorySubtree)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryTreeID` | path | `string` | yes | The unique identifier of the eBay category tree. The category tree ID for an eBay marketplace can be retrieved using the "Get Default Category Tree" action. |
| `category_id` | query | `string` | yes | The unique identifier of the category at the top of the subtree being requested. Metadata on this category and all its descendant categories are retrieved.  Note: If the category_id submitted identifies a leaf node of the tree, the call response will contain information about only that leaf node, which is a valid subtree. |
