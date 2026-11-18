# Brightpearl: Create Goods-Out Notes



```
POST https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-goods-out-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-goods-out-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-goods-out-notes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes |  |
| `warehouses[]` | array<object> | no |  |
| `warehouses[].warehouseId` | number | no |  |
| `warehouses[].products[]` | array<object> | no |  |
| `warehouses[].products[].productId` | number | no |  |
| `warehouses[].products[].salesOrderRowId` | number | no |  |
| `warehouses[].products[].quantity` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `warehouses[].releaseDate` | date | no |  |
| `warehouses[].transfer` | boolean | no |  |
| `priority` | boolean | no |  |
| `shippingMethodId` | number | no |  |
| `labelUri` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `POST /warehouse-service/order/:orderId/goods-note/goods-out` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-goods-out-notes.md) for the provider-specific parameters and requirements.

