# Get Category Tree with eBay

Retrieves a complete category tree by its ID.

## Endpoint

- **Method:** `GET`
- **Path:** `commerce/taxonomy/v1/category_tree/:categoryTreeID`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Get Category Tree](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getCategoryTree)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryTreeID` | path | `string` | yes | The unique identifier of the eBay category tree. The category tree ID for an eBay marketplace can be retrieved using the "Get Default Category Tree" action. |
