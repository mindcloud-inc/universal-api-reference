# Get Category Suggestions with eBay

Retrieve a categories that are considered by eBay to most closely correspond to the provided query.

## Endpoint

- **Method:** `GET`
- **Path:** `commerce/taxonomy/v1/category_tree/0/get_category_suggestions`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Get Category Suggestions](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getCategorySuggestions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | A quoted string that describes or characterizes the item being offered for sale. The string format is free form, and can contain any combination of phrases or keywords. eBay will parse the string and return suggested categories for the item. |
