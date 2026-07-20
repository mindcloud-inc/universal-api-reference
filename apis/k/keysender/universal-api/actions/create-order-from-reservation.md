# Keysender: Create Order From Reservation

Creates an order from a Keysender reservation.

```
POST https://connect.mindcloud.co/v1/universal/keysender/latest/actions/create-order-from-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/create-order-from-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/create-order-from-reservation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reservationId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "orderId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Order status message. |
| `orderId` | string | Order identifier. |
| `status` | string | Order status. |

## Native endpoint

Through the native Keysender API, this operation is `POST /catalog/order` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-from-reservation.md) for the provider-specific parameters and requirements.

