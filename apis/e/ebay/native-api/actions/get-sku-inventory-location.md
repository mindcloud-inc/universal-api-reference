# Get SKU Inventory Location with eBay

Allows sellers to retrieve the locations mapped to a specific SKU within a listing.

## Endpoint

- **Method:** `GET`
- **Path:** `sell/inventory/v1/listing/:listingID/sku/:sku/locations`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Get SKU Inventory Location](https://developer.ebay.com/api-docs/sell/inventory/resources/listing/methods/getSkuLocationMapping)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingID` | query | `string` | yes | The unique-id of the listing that the SKU belongs to for which all mapped locations will be retrieved. |
| `sku` | query | `string` | yes | The seller-defined SKU value of the item/variation for which location mappings will be retrieved. This SKU value must be defined in the listing specified in the 'Listing ID' parameter above. |
