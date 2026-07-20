# SquareSpace: Fulfill Order

Updates order fulfillments in Squarespace.

```
PUT https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/fulfill-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/fulfill-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "shipments[]": [
    {}
  ],
  "shipments[].carrierName": "Ava Chen",
  "shipments[].service": "string",
  "shipments[].shipDate": "string",
  "shipments[].trackingNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/fulfill-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "shipments[]": [{}],
    "shipments[].carrierName": "Ava Chen",
    "shipments[].service": "string",
    "shipments[].shipDate": "string",
    "shipments[].trackingNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<string> | yes | Order ID to fulfill. |
| `shipments[]` | array<object> | yes | List of shipment payload objects. |
| `shipments[].carrierName` | string | yes | Carrier name. |
| `shipments[].service` | string | yes | Carrier service level. |
| `shipments[].shipDate` | string | yes | Shipment datetime in ISO 8601 UTC. |
| `shipments[].trackingNumber` | string | yes | Parcel tracking number. |
| `shipments[].trackingUrl` | string | no | Carrier tracking URL. |
| `shouldSendNotification` | boolean | no | Send shipment email notification to customer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SquareSpace API returns.

## Native endpoint

Through the native SquareSpace API, this operation is `POST /1.0/commerce/orders/:id/fulfillments` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fulfill-order.md) for the provider-specific parameters and requirements.

