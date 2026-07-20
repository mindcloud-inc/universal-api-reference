# Big Cartel: Update Shipment

Updates a shipment for a Big Cartel order.

```
PUT https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/update-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/update-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "orderId": "string",
  "shipmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/update-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "orderId": "string",
    "shipmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Big Cartel account ID. |
| `orderId` | string | yes | The Big Cartel order ID. |
| `shipmentId` | string | yes | The Big Cartel shipment ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Big Cartel API returns.

## Native endpoint

Through the native Big Cartel API, this operation is `PATCH /v1/accounts/[:account-id]/orders/[:order-id]/shipments/[:shipment-id]` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipment.md) for the provider-specific parameters and requirements.

