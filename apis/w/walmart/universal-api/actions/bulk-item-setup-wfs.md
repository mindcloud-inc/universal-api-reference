# Walmart: Bulk Item Setup - WFS

This API is used for converting existing Marketplace items to be WFS eligible.

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-wfs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-wfs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedType": "OMNI_WFS"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-wfs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedType": "OMNI_WFS"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedType` | string | yes | Allowed: `OMNI_WFS` Default: `OMNI_WFS`. |
| `MPItem[].Orderable` | object | no |  |
| `MPItem[].Orderable.productIdentifiers.productIdType` | string | no | example: "GTIN" or "UPC" etc. |
| `MPItem[].Orderable.sku` | string | no |  |
| `MPItem[].tradeItem.sku` | string | no |  |
| `MPItem[].Visible.brand` | string | no |  |
| `MPItem[].Orderable.productIdentifiers` | object | no |  |
| `MPItem[].Orderable.productIdentifiers.productId` | string | no |  |
| `MPItem[].ptCategoryLabel` | list<string> | no |  |
| `MPItem[].Visible.productName` | string | no |  |
| `MPItem[]` | array | no |  |
| `MPItem[].Orderable.country_of_origin_substantial_transformation` | list | no | The country where the item and/or its components are manufactured, produced, or grown. |
| `MPItem[].Visible` | object | no |  |
| `MPItem[].Visible.isProp65WarningRequired` | string | no | "Yes" or "No" |
| `MPItem[].Orderable.price` | number | no |  |
| `MPItem[].tradeItem` | object | no |  |
| `MPItem[].Visible.mainImageUrl` | string | no |  |
| `MPItem[].Orderable.ShippingWeight` | number | no |  |
| `MPItem[].Visible.condition` | string | no |  |
| `MPItemFeedHeader.subCategory` | string | no | Example: `hair_accessories`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `MPItemFeedHeader.locale` | string | no | Default: `en`. |
| `MPItemFeedHeader` | object | no |  |
| `MPItemFeedHeader.version` | string | no | Allowed Value: `4.8` This spec version is passed to the Taxonomy API to provide you with a list of Category options to choose from. Specifying a version other than the allowed value above may result in errors when you submit your request. Default: `1.4`. |
| `MPItemFeedHeader.sellingChannel` | string | no | Default: `fbw`. |
| `MPItemFeedHeader.businessUnit` | list<string> | no | Enter a specific subcategoryId of the chosen Category. Defaults to the selected Categories `categoryId` below if not set. One of: `ASDA_GM`, `SAMSCLUB`, `WALMART_CA`, `WALMART_US`. |
| `MPItemFeedHeader.subset` | string | no | Default: `EXTERNAL`. |

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

Through the native Walmart API, this operation is `POST /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-item-setup-wfs.md) for the provider-specific parameters and requirements.

