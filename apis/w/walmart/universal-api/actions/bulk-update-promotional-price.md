# Walmart: Bulk Update Promotional Price

Create, update, or delete promotional prices for multiple SKUs.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-update-promotional-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-update-promotional-price" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedType": "PRICE_AND_PROMOTION"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-update-promotional-price', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedType": "PRICE_AND_PROMOTION"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `MPItem[]` | array<object> | no |  |
| `MPItem[].promotionInformation.promotionSettingAction` | list<string> | no | The action to apply to promotions for this SKU. |
| `MPItem[].sku` | string | no | **required** The seller-defined Stock Keeping Unit (SKU) for the item being updated. |
| `MPItemFeedHeader.locale` | list<string> | no | **required** The market specific locale. Allowed values by market include: - `en` for US - `es` for MX & CL - `en` & `fr` for CA. - Market availability: Global Default: `en`. |
| `MPItem[].price` | number | no | **required** The current selling price of the item on Walmart.com. |
| `MPItem[].promotionInformation.promotionPrice` | number | no | The promotional price for the item during the promotion window. |
| `MPItemFeedHeader.version` | list<string> | no | **required** The feed schema version. The values vary by region. Allowed values: - `2.0.20240126-12_25_52-api` for U.S. - `5.0.20250328-17_43_36-api` for CA, MX and CL. __Market availability: Global__ Default: `2.0.20240126-12_25_52-api`. |
| `MPItem[].msrp` | number | no | The manufacturer's suggested retail price (MSRP) for the item. |
| `MPItem[].promotionInformation.promotionType` | list<string> | no | The promotion type to apply. |
| `MPItemFeedHeader.businessUnit` | list<string> | no | Business unit identifier matching the target market. For example, use WALMART_US for the US market. __Market availability: US__ Default: `WALMART_US`. |
| `MPItem[].promoid` | string | no | The promotion identifier. Provide this if updating or deleting an existing promotion. |
| `MPItem[].promotionInformation.promotionPlacement` | list<string> | no | Indicates where a promotion is applied or displayed. Allowed: `MAP Cart` __Market availability: US__ |
| `MPItemFeedHeader.mart` | string | no | The mart ID for the various markets are: - WALMART_CA for CA - WALMART_MEXICO for MX - WALMART_CHILE for CL.. __Market availability: CA \| MX \| CL__ |
| `MPItem[].promotionInformation` | object | no |  |
| `MPItem[].promotionInformation.promotionPriceStartDateTime` | string | no | The UTC date and time when the promotional price becomes effective. |
| `MPItemFeedHeader.subset` | string | no | Origin of the data. Use `EXTERNAL` for partner submitted feeds. __Market availability: CA \| MX \| CL__ |
| `MPItem[].promotionInformation.promotionPriceEndDateTime` | string | no | The UTC date and time when the promotional price ends. |
| `MPItemFeedHeader.tenant` | string | no | The tenant identifier for the marketplace. For example, use: - `WALMART_CA` for CA - `WALMART_MEXICO` for MX - `WALMART_CHILE` for CL. __Market availability: CA \| MX \| CL__ |
| `MPItemFeedHeader.feedType` | string | no | The type of feed for this request. Allowed Value: `PRICE_AND_PROMOTION` __Market availability: CA \| MX \| CL__ |
| `MPItemFeedHeader.subCategory` | string | no | ItemFeed subcategory for price update. Market availability: CA \| MX \| CL |
| `MPItemFeedHeader.processMode` | string | no | The feed processing behavior. Use `REPLACE` to overwrite existing values. __Market availability: CA \| MX \| CL__ |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedType` | string | yes | The feed Type. Allowed Value: `PRICE_AND_PROMOTION` __Market Availability: Global__ Default: `PRICE_AND_PROMOTION`. Example: `PRICE_AND_PROMOTION`. |
| `MPItemFeedHeader` | object | no | Defaults to US Marketplace settings. For CA, MX and CL, all fields except ("businessUnit") are required. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Walmart API returns.

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-promotional-price.md) for the provider-specific parameters and requirements.

