# PassKit Event Tickets: Create Ticket By Id

Creates a new ticket in PassKit by user-defined IDs.

```
POST https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/create-ticket-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/create-ticket-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/create-ticket-by-id', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "eventId": "string",
      "id": "string",
      "orderNumber": "string",
      "status": "string",
      "ticketNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventId` | string |  |
| `id` | string |  |
| `orderNumber` | string |  |
| `status` | string |  |
| `ticketNumber` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `POST /eventTickets/ticket/id` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-by-id.md) for the provider-specific parameters and requirements.

