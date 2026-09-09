# Bulk Item Setup - WFS with Walmart

This API is used for converting existing Marketplace items to be WFS eligible.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Item Setup - WFS](https://developer.walmart.com/us-marketplace/reference/itembulkuploads)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `string` | yes | Allowed: `OMNI_WFS` |
| `MPItem[].Orderable` | body | `object` | no | — |
| `MPItem[].Orderable.productIdentifiers.productIdType` | body | `string` | no | example: "GTIN" or "UPC" etc. |
| `MPItem[].Orderable.sku` | body | `string` | no | — |
| `MPItem[].tradeItem.sku` | body | `string` | no | — |
| `MPItem[].Visible.brand` | body | `string` | no | — |
| `MPItemFeedHeader.locale` | body | `string` | no | — |
| `MPItem[].Orderable.productIdentifiers` | body | `object` | no | — |
| `MPItem[].Orderable.productIdentifiers.productId` | body | `string` | no | — |
| `MPItem[].ptCategoryLabel` | body | `list<string>` | no | — |
| `MPItem[].Visible.productName` | body | `string` | no | — |
| `MPItemFeedHeader` | body | `object` | no | — |
| `MPItemFeedHeader.version` | body | `string` | no | Allowed Value: `4.8`  This spec version is passed to the Taxonomy API to provide you with a list of Category options to choose from. Specifying a version other than the allowed value above may result in errors when you submit your request. |
| `MPItem[]` | body | `array` | no | — |
| `MPItem[].Orderable.country_of_origin_substantial_transformation` | body | `list` | no | The country where the item and/or its components are manufactured, produced, or grown. |
| `MPItem[].Visible` | body | `object` | no | — |
| `MPItem[].Visible.isProp65WarningRequired` | body | `string` | no | "Yes" or "No" |
| `MPItemFeedHeader.sellingChannel` | body | `string` | no | — |
| `MPItem[].Orderable.price` | body | `number` | no | — |
| `MPItem[].tradeItem` | body | `object` | no | — |
| `MPItem[].Visible.mainImageUrl` | body | `string` | no | — |
| `MPItemFeedHeader.businessUnit` | body | `list<string>` | no | Enter a specific subcategoryId of the chosen Category. Defaults to the selected Categories `categoryId` below if not set. Accepted values: `ASDA_GM`, `SAMSCLUB`, `WALMART_CA`, `WALMART_US`. |
| `MPItem[].Orderable.ShippingWeight` | body | `number` | no | — |
| `MPItem[].Visible.condition` | body | `string` | no | — |
| `MPItemFeedHeader.subset` | body | `string` | no | — |
| `MPItemFeedHeader.subCategory` | body | `string` | no | — |
