# Cratejoy: Update Product

Updates an existing product in Cratejoy.

```
PUT https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | The Cratejoy product ID. |
| `name` | string | no | The product name. |
| `shipWeight` | number | no | The product shipping weight. |
| `visible` | boolean | no | Whether the product is visible. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "listed": true,
      "name": "Ava Chen",
      "ship_weight": 1,
      "sku": "string",
      "type": "string",
      "url": "https://example.com",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `listed` | boolean |  |
| `name` | string |  |
| `ship_weight` | number |  |
| `sku` | string |  |
| `type` | string |  |
| `url` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Cratejoy API, this operation is `PUT /v1/products/:productId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

