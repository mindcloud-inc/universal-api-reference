# List Offers by SKU with eBay

Retrieves all existing offers for the specified SKU value. With options to limit the retrieved offers to a specific eBay marketplace, or a listing format.

## Endpoint

- **Method:** `GET`
- **Path:** `sell/inventory/v1/offer`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [List Offers by SKU](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/getOffers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | query | `string` | yes | The seller-defined SKU value. All offers associated with this product are returned in the response. |
| `format` | query | `string` | no | This value sets the listing format for the offers being retrieved. Pass this parameter when you only want to see offers in a specified listing format, such as FIXED_PRICE or AUCTION. |
| `marketplace_id` | query | `list<string>` | no | — |
