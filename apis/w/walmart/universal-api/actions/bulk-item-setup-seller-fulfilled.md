# Walmart: Bulk Item Setup - Seller Fulfilled

This API updates items in bulk (max: 10,000 items per request)

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-seller-fulfilled
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-seller-fulfilled" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedType": "MP_ITEM",
  "MPItemFeedHeader.version": "5.0.20260330-14_47_14-api"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-seller-fulfilled', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedType": "MP_ITEM",
    "MPItemFeedHeader.version": "5.0.20260330-14_47_14-api"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedType` | string | yes | The type of feed specifies the nature of the update. Choosing `MP_ITEM` indicates Seller Fulfilled Item set up. Allowed: `MP_ITEM` Default: `MP_ITEM`. |
| `MPItem[].Orderable.productIdentifiers.productIdType` | string | no | example: "GTIN" |
| `MPItem[].ptCategoryLabel` | list<string> | no |  |
| `MPItem[].Visible.productName` | string | no |  |
| `MPItemFeedHeader.businessUnit` | list<string> | no | Enter a specific subcategoryId of the chosen Category. Defaults to the selected Categories `categoryId` below if not set. One of: `ASDA_GM`, `SAMSCLUB`, `WALMART_CA`, `WALMART_US`. |
| `MPItem[].Orderable` | object | no |  |
| `MPItem[].Orderable.productIdentifiers.productId` | string | no |  |
| `MPItem[].Visible.brand` | string | no |  |
| `MPItemFeedHeader` | object | no |  |
| `MPItemFeedHeader.locale` | string | no | Default: `en`. |
| `MPItem[]` | array | no |  |
| `MPItem[].Orderable.sku` | string | no |  |
| `MPItem[].Visible` | object | no |  |
| `MPItem[].Visible.shortDescription` | string | no |  |
| `MPItemFeedHeader.version` | string | yes | Allowed Value: `4.8` This spec version is passed to the Taxonomy API to provide you with a list of Category options to choose from. Specifying a version other than the allowed value above may result in errors when you submit your request. Default: `5.0.20260330-14_47_14-api`. |
| `MPItem[].Orderable.productIdentifiers` | object | no |  |
| `MPItem[].Visible.keyFeatures[]` | array<string> | no | use: @generated |
| `MPItem[].Orderable.country_of_origin_substantial_transformation` | list | no | The country where the item and/or its components are manufactured, produced, or grown. |
| `MPItem[].Visible.mainImageUrl` | string | no |  |
| `MPItem[].Orderable.price` | number | no |  |
| `MPItem[].Visible.isProp65WarningRequired` | string | no |  |
| `MPItem[].Orderable.ShippingWeight` | number | no |  |
| `MPItem[].Visible.condition` | string | no |  |
| `MPItem[].Visible.hasWrittenwarranty` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feedId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-item-setup-seller-fulfilled.md) for the provider-specific parameters and requirements.

