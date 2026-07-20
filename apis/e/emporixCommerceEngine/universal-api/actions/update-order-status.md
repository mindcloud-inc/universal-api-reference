# Emporix Commerce Engine: Update Order Status

Updates a sales order status in Emporix Commerce Engine.

```
PUT https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/update-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/update-order-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/update-order-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | The unique ID of the sales order whose status should be updated. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Emporix Commerce Engine API returns.

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /order-v2/{{credentials.tenantId}}/salesorders/:orderId/transitions` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-status.md) for the provider-specific parameters and requirements.

