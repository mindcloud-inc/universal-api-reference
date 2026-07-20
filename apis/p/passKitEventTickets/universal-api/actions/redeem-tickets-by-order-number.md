# PassKit Event Tickets: Redeem Tickets By Order Number

Redeems tickets by order number in PassKit.

```
PUT https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/redeem-tickets-by-order-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/redeem-tickets-by-order-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/redeem-tickets-by-order-number', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "orderNumber": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `orderNumber` | string |  |
| `status` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `PUT /eventTickets/tickets/orderNumber/redeem` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redeem-tickets-by-order-number.md) for the provider-specific parameters and requirements.

