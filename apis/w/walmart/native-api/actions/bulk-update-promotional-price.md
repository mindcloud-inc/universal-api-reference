# Bulk Update Promotional Price with Walmart

Create, update, or delete promotional prices for multiple SKUs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Update Promotional Price](https://developer.walmart.com/global-marketplace/reference/pricebulkuploads)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `string` | yes | The feed Type. Allowed Value: `PRICE_AND_PROMOTION`  __Market Availability: Global__ |
| `MPItem[]` | body | `array<object>` | no | — |
| `MPItem[].promotionInformation.promotionSettingAction` | body | `list<string>` | no | The action to apply to promotions for this SKU. |
| `MPItem[].sku` | body | `string` | no | **required** The seller-defined Stock Keeping Unit (SKU) for the item being updated. |
| `MPItemFeedHeader.locale` | body | `list<string>` | no | **required** The market specific locale. Allowed values by market include: - `en` for US - `es` for MX & CL - `en` & `fr` for CA. - Market availability: Global |
| `MPItem[].price` | body | `number` | no | **required** The current selling price of the item on Walmart.com. |
| `MPItem[].promotionInformation.promotionPrice` | body | `number` | no | The promotional price for the item during the promotion window. |
| `MPItemFeedHeader` | body | `object` | no | Defaults to US Marketplace settings. For CA, MX and CL, all fields except ("businessUnit") are required. |
| `MPItemFeedHeader.version` | body | `list<string>` | no | **required** The feed schema version. The values vary by region. Allowed values: - `2.0.20240126-12_25_52-api` for U.S. - `5.0.20250328-17_43_36-api` for CA, MX and CL.  __Market availability: Global__ |
| `MPItem[].msrp` | body | `number` | no | The manufacturer's suggested retail price (MSRP) for the item. |
| `MPItem[].promotionInformation.promotionType` | body | `list<string>` | no | The promotion type to apply. |
| `MPItemFeedHeader.businessUnit` | body | `list<string>` | no | Business unit identifier matching the target market. For example, use WALMART_US for the US market.  __Market availability: US__ |
| `MPItem[].promoid` | body | `string` | no | The promotion identifier. Provide this if updating or deleting an existing promotion. |
| `MPItem[].promotionInformation.promotionPlacement` | body | `list<string>` | no | Indicates where a promotion is applied or displayed. Allowed: `MAP Cart`  __Market availability: US__ |
| `MPItemFeedHeader.mart` | body | `string` | no | The mart ID for the various markets are: - WALMART_CA for CA - WALMART_MEXICO for MX - WALMART_CHILE for CL.. __Market availability: CA \| MX \| CL__ |
| `MPItem[].promotionInformation` | body | `object` | no | — |
| `MPItem[].promotionInformation.promotionPriceStartDateTime` | body | `string` | no | The UTC date and time when the promotional price becomes effective. |
| `MPItemFeedHeader.subset` | body | `string` | no | Origin of the data. Use `EXTERNAL` for partner submitted feeds.   __Market availability: CA \| MX \| CL__ |
| `MPItem[].promotionInformation.promotionPriceEndDateTime` | body | `string` | no | The UTC date and time when the promotional price ends. |
| `MPItemFeedHeader.tenant` | body | `string` | no | The tenant identifier for the marketplace. For example, use: - `WALMART_CA` for CA - `WALMART_MEXICO` for MX - `WALMART_CHILE` for CL.   __Market availability: CA \| MX \| CL__ |
| `MPItemFeedHeader.feedType` | body | `string` | no | The type of feed for this request. Allowed Value: `PRICE_AND_PROMOTION`  __Market availability: CA \| MX \| CL__ |
| `MPItemFeedHeader.subCategory` | body | `string` | no | ItemFeed subcategory for price update. Market availability: CA \| MX \| CL |
| `MPItemFeedHeader.processMode` | body | `string` | no | The feed processing behavior. Use `REPLACE` to overwrite existing values.  __Market availability: CA \| MX \| CL__ |
