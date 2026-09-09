# Bulk Item Setup - Seller Fulfilled with Walmart

This API updates items in bulk (max: 10,000 items per request)

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Item Setup - Seller Fulfilled](https://developer.walmart.com/us-marketplace/reference/itembulkuploads)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `string` | yes | The type of feed specifies the nature of the update. Choosing `MP_ITEM` indicates Seller Fulfilled Item set up.  Allowed: `MP_ITEM` |
| `MPItem[].Orderable.productIdentifiers.productIdType` | body | `string` | no | example: "GTIN" |
| `MPItem[].ptCategoryLabel` | body | `list<string>` | no | — |
| `MPItem[].Visible.productName` | body | `string` | no | — |
| `MPItemFeedHeader.businessUnit` | body | `list<string>` | no | Enter a specific subcategoryId of the chosen Category. Defaults to the selected Categories `categoryId` below if not set. Accepted values: `ASDA_GM`, `SAMSCLUB`, `WALMART_CA`, `WALMART_US`. |
| `MPItem[].Orderable` | body | `object` | no | — |
| `MPItem[].Orderable.productIdentifiers.productId` | body | `string` | no | — |
| `MPItem[].Visible.brand` | body | `string` | no | — |
| `MPItemFeedHeader` | body | `object` | no | — |
| `MPItemFeedHeader.locale` | body | `string` | no | — |
| `MPItem[]` | body | `array` | no | — |
| `MPItem[].Orderable.sku` | body | `string` | no | — |
| `MPItem[].Visible` | body | `object` | no | — |
| `MPItem[].Visible.shortDescription` | body | `string` | no | — |
| `MPItemFeedHeader.version` | body | `string` | yes | Allowed Value: `4.8`  This spec version is passed to the Taxonomy API to provide you with a list of Category options to choose from. Specifying a version other than the allowed value above may result in errors when you submit your request. |
| `MPItem[].Orderable.productIdentifiers` | body | `object` | no | — |
| `MPItem[].Visible.keyFeatures[]` | body | `array<string>` | no | use: @generated |
| `MPItem[].Orderable.country_of_origin_substantial_transformation` | body | `list` | no | The country where the item and/or its components are manufactured, produced, or grown. |
| `MPItem[].Visible.mainImageUrl` | body | `string` | no | — |
| `MPItem[].Orderable.price` | body | `number` | no | — |
| `MPItem[].Visible.isProp65WarningRequired` | body | `string` | no | — |
| `MPItem[].Orderable.ShippingWeight` | body | `number` | no | — |
| `MPItem[].Visible.condition` | body | `string` | no | — |
| `MPItem[].Visible.has_written_warranty` | body | `string` | no | — |
