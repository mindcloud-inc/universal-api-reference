# PassKit Event Tickets: List Tickets By Order Number

Retrieves tickets by order number from PassKit.

```
GET https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/list-tickets-by-order-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/list-tickets-by-order-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/list-tickets-by-order-number?${params}`, {
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
| `orderNumber` | string | no | Order number whose tickets you want to list. |
| `productionId` | string | no | Filter order-number ticket lookup by production id. |
| `productionUid` | string | no | Filter order-number ticket lookup by production uid. |

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

Through the native PassKit Event Tickets API, this operation is `GET /eventTickets/tickets/orderNumber` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets-by-order-number.md) for the provider-specific parameters and requirements.

