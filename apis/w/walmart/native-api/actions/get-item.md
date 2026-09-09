# Get Item with Walmart

Retrieved detailed information about a specific item from the partner's catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/items/:id`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Item](https://developer.walmart.com/us-marketplace/reference/getanitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A unique seller-specified identifier for the item. Defaults to the SKU code. |
| `productIdType` | query | `list<string>` | no | Search by additional supported product identifiers (SKU, GTIN, EAN, ISBN, EAN, and Item ID). Use this parameter if you need to filter results based on a specific product ID type. If not specified, the call searches by SKU by default. |
| `condition` | query | `list<string>` | no | Indicates the condition of the product. Specify this parameter to filter items based on their condition. |
| `availability` | query | `list<string>` | no | Specifies the product's availability status. Use this parameter to filter items by their availability status. |
| `showDuplicateItemDetails` | query | `boolean` | no | Toggle on to receive information on duplicate items. Format: `toggle`. |
| `includeCustomerFavoritesStatus` | query | `boolean` | no | Toggle on to include `isCustomerFavorite` item details in the response. Format: `toggle`. |
