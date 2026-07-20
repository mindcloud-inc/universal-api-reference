# Shipday: Unassign Order from Driver

Unassigns an existing order from a driver in Shipday.

```
PUT https://connect.mindcloud.co/v1/universal/shipday/latest/actions/unassign-order-from-driver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/unassign-order-from-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "44865172"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipday/latest/actions/unassign-order-from-driver', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "44865172"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | Shipday order ID used in the request path. Example: `44865172`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider message returned after unassignment. |
| `success` | boolean | Whether the carrier removal succeeded. |

## Native endpoint

Through the native Shipday API, this operation is `PUT /orders/unassign/:orderId` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unassign-order-from-driver.md) for the provider-specific parameters and requirements.

