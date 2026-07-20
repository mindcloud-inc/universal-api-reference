# Pinterest: Operate On Product Pins

Operates on Pinterest catalog items in batch.

```
PUT https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/operate-on-product-pins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/operate-on-product-pins" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/operate-on-product-pins', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[].attributes.shipping` | string | no |  |
| `items[].attributes.shippingHeight` | string | no |  |
| `items[].attributes.shippingWeight` | string | no |  |
| `items[].attributes.shippingWidth` | string | no |  |
| `items[].attributes.size` | string | no |  |
| `items[].attributes.sizeSystem` | string | no |  |
| `items[].attributes.tax` | string | no |  |
| `items[].attributes.title` | string | no |  |
| `items[].attributes.variantNames` | string | no |  |
| `items[].attributes.variantValues` | string | no |  |
| `adAccountId` | string | no |  |
| `items[].attributes.imageLink` | object<string> | no |  |
| `items[].operation` | list | no |  |
| `catalogType` | list | no |  |
| `items[].attributes` | object | no |  |
| `items[].attributes.videoLink` | string | no |  |
| `country` | string | no |  |
| `items[].attributes.additionalImageLink` | object<string> | no |  |
| `items[].itemId` | string | no |  |
| `items[].attributes.adLink` | string | no |  |
| `language` | string | no |  |
| `items[]` | array | no |  |
| `items[].attributes.adult` | string | no |  |
| `items[].attributes.ageGroup` | string | no |  |
| `items[].attributes.availability` | string | no |  |
| `items[].attributes.averageReviewRating` | string | no |  |
| `items[].attributes.brand` | string | no |  |
| `items[].attributes.color` | string | no |  |
| `items[].attributes.condition` | string | no |  |
| `items[].attributes.customLabel0` | string | no |  |
| `items[].attributes.customLabel1` | string | no |  |
| `items[].attributes.CustomLabel3` | string | no |  |
| `items[].attributes.customLabel2` | string | no |  |
| `items[].attributes.customLabel4` | string | no |  |
| `items[].attributes.customLabel5` | string | no |  |
| `items[].attributes.description` | string | no |  |
| `items[].attributes.freeShippingLabel` | string | no |  |
| `items[].attributes.freeShippingLimit` | string | no |  |
| `items[].attributes.gender` | string | no |  |
| `items[].attributes.googleProductCategory` | string | no |  |
| `items[].attributes.gtin` | string | no |  |
| `items[].attributes.itemGroupId` | string | no |  |
| `items[].attributes.lastUpdatedTime` | string | no |  |
| `items[].attributes.link` | string | no |  |
| `items[].attributes.material` | string | no |  |
| `items[].attributes.minimumAdPrice` | string | no |  |
| `items[].attributes.mobileLink` | string | no |  |
| `items[].attributes.mpn` | string | no |  |
| `items[].attributes.numberOfRatings` | string | no |  |
| `items[].attributes.numberOfReviews` | string | no |  |
| `items[].attributes.pattern` | string | no |  |
| `items[].attributes.price` | string | no |  |
| `items[].attributes.productType` | string | no |  |
| `items[].attributes.salePrice` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `POST catalogs/items/batch` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/operate-on-product-pins.md) for the provider-specific parameters and requirements.

