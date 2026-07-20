# WeForest: Update order item

Updates an existing tree-planting order item in WeForest.

```
PUT https://connect.mindcloud.co/v1/universal/weForest/latest/actions/update-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/update-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "itemId": 1,
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weForest/latest/actions/update-order-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "itemId": 1,
    "quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | Order identifier from WeForest. |
| `itemId` | number | yes | Order item identifier from WeForest. |
| `quantity` | number<object> | yes | Updated quantity for this order item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "orderId": 1,
      "product": {},
      "quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `orderId` | number |  |
| `product` | object |  |
| `quantity` | number |  |

## Native endpoint

Through the native WeForest API, this operation is `PATCH /trees/:orderId/items/:itemId` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-item.md) for the provider-specific parameters and requirements.

