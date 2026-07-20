# WeForest: Get order item

Retrieves a tree-planting order item from WeForest.

```
GET https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-order-item?connectionId=$CONNECTION_ID&orderId=1&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1",
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-order-item?${params}`, {
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
| `orderId` | number | yes | Order identifier from WeForest. |
| `itemId` | number | yes | Order item identifier from WeForest. |

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

Through the native WeForest API, this operation is `GET /trees/:orderId/items/:itemId` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-item.md) for the provider-specific parameters and requirements.

