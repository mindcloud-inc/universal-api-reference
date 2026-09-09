# Bulk Update Price ( New ) with Walmart

Update the price section in bulk for multiple items. This is useful for implementing pricing strategies across your catalog, such as seasonal discounts, competitive pricing adjustments, or clearance sales.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Update Price ( New )](https://developer.walmart.com/us-marketplace/reference/pricebulkuploads-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MPItem[].sku` | body | `string` | no | The SKU of the item for which the price is being updated. |
| `MPItemFeedHeader` | body | `object` | no | — |
| `MPItemFeedHeader.businessUnit` | body | `list<list>` | no | The business unit for which the feed is submitted. For example, use 'Walmart_US' for U.S. Marketplace. |
| `MPItem[].price` | body | `number` | no | The selling price of the item on Walmart.com. |
| `MPItemFeedHeader.version` | body | `list<string>` | no | The version of the feed schema being used. Please use `5.0.20250328-17_43_36-api` for the PRICE section updates and use `2.0.20240126-12_25_52-api` for PROMO&DISCOUNT section updates. |
| `MPItem[]` | body | `array<object>` | no | Add (+) or map items here from a previous step. |
| `MPItem[].msrp` | body | `number` | no | The manufacturer's suggested retail price (MSRP) for the item. |
| `MPItemFeedHeader.locale` | body | `string` | no | The locale code for the content in the feed.  For example, `en` for English. |
| `MPItem[].businessPrice` | body | `number` | no | The business price for the item. Unlike the `price` field, which is visible to everyone, the `businessPrice` is only visible to verified business organizations and non-profits. In the Walmart ecosystem, setting a `businessPrice` that is lower than your standard retail price can help you: - Win the Business Buy Box - Encourage Bulk Purchasing from retailers. |
