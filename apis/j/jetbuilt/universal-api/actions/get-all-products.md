# Jetbuilt: Get All Products



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-all-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-all-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-all-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | no |  |
| `min_updated_at` | string | no |  |
| `max_updated_at` | string | no |  |
| `manufactuer_name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "custom": true,
      "depthUnit": "string",
      "depthValue": "string",
      "directPricing": true,
      "discontinued": true,
      "favorite": true,
      "heatLoadUnit": "string",
      "heatLoadValue": "string",
      "heightUnit": "string",
      "heightValue": "string",
      "id": 1,
      "imageUrl": "https://example.com",
      "manufacturer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "mapp": "string",
      "model": "string",
      "msrp": "string",
      "notes": "string",
      "phaseId": 1,
      "poeUnit": "string",
      "poeValue": "string",
      "powerUnit": "string",
      "powerValue": "string",
      "price": "string",
      "productId": 1,
      "rackUnit": "string",
      "rackValue": "string",
      "shippingCost": "string",
      "shippingPrice": "string",
      "shortDescription": "string",
      "taxEquipment": true,
      "taxLabor": true,
      "taxShipping": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "warrantyUnit": "string",
      "warrantyValue": "string",
      "weightUnit": "string",
      "weightValue": "string",
      "widthUnit": "string",
      "widthValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | string |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `custom` | boolean |  |
| `depthUnit` | string |  |
| `depthValue` | string |  |
| `directPricing` | boolean |  |
| `discontinued` | boolean |  |
| `favorite` | boolean |  |
| `heatLoadUnit` | string |  |
| `heatLoadValue` | string |  |
| `heightUnit` | string |  |
| `heightValue` | string |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `manufacturer.id` | number |  |
| `manufacturer.name` | string |  |
| `mapp` | string |  |
| `model` | string |  |
| `msrp` | string |  |
| `notes` | string |  |
| `phaseId` | number |  |
| `poeUnit` | string |  |
| `poeValue` | string |  |
| `powerUnit` | string |  |
| `powerValue` | string |  |
| `price` | string |  |
| `productId` | number |  |
| `rackUnit` | string |  |
| `rackValue` | string |  |
| `shippingCost` | string |  |
| `shippingPrice` | string |  |
| `shortDescription` | string |  |
| `taxEquipment` | boolean |  |
| `taxLabor` | boolean |  |
| `taxShipping` | boolean |  |
| `updatedAt` | date |  |
| `warrantyUnit` | string |  |
| `warrantyValue` | string |  |
| `weightUnit` | string |  |
| `weightValue` | string |  |
| `widthUnit` | string |  |
| `widthValue` | string |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET product_databases/:databaseId/products` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-products.md) for the provider-specific parameters and requirements.

