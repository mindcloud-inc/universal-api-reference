# Jetbuilt: Create a Product



```
POST https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-a-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-a-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productDatabaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-a-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productDatabaseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commodityCode` | string | no |  |
| `cost` | number | no |  |
| `countryOfOrigin` | string | no |  |
| `currencyCode` | string | no |  |
| `depthUnit` | string | no | Possible values: in, ft, cm, mm |
| `depthValue` | number | no |  |
| `favorite` | string | no |  |
| `heatLoadUnit` | string | no | Possible values: BTU |
| `heatLoadValue` | string | no |  |
| `heightUnit` | string | no | Possible values: in, ft, cm, mm |
| `heightValue` | number | no |  |
| `image` | string | no |  |
| `notes` | string | no |  |
| `phaseId` | string | no |  |
| `poeUnit` | string | no | Possible values: W |
| `poeValue` | number | no |  |
| `powerUnit` | string | no | Possible values: W |
| `powerValue` | number | no |  |
| `Price` | number | no |  |
| `productId` | number | no |  |
| `rackUnit` | string | no | Possible values: RU |
| `rackValue` | number | no |  |
| `shippingCost` | string | no |  |
| `shippingDepthUnit` | string | no | Possible values: in, ft, cm, mm |
| `shippingDepthValue` | number | no |  |
| `shippingHeightUnit` | string | no | Possible values: in, ft, cm, mm |
| `shippingHeightValue` | number | no |  |
| `shippingPrice` | number | no |  |
| `shippingWeightUnit` | string | no | Possible values: lb, oz, kg, g |
| `shippingWeightValue` | number | no |  |
| `shippingWidthUnit` | string | no | Possible values: in, ft, cm, mm |
| `shippingWidthValue` | number | no |  |
| `shortDescription` | string | no |  |
| `taxEquipment` | boolean | no |  |
| `taxLabor` | boolean | no |  |
| `taxShipping` | boolean | no |  |
| `warrantyUnit` | string | no | Possible values: d, mo, yr |
| `warrantyValue` | number | no | The warranty value in days months or years (decimal) |
| `weightUnit` | string | no | Possible values: lb, oz, kg, g |
| `weightValue` | number | no |  |
| `widthUnit` | string | no | Possible values: in, ft, cm, mm |
| `widthValue` | number | no |  |
| `productDatabaseId` | string | yes |  |
| `manufacturerName` | string | no |  |
| `model` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `POST product_databases/:productDatabaseId/products` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-product.md) for the provider-specific parameters and requirements.

