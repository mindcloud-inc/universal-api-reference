# PassKit Event Tickets: Get Ticket By Ticket Number

Retrieves a ticket by ticket number from PassKit.

```
GET https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-ticket-by-ticket-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-ticket-by-ticket-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-ticket-by-ticket-number?${params}`, {
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
| `productionId` | string | no | Filter the ticket lookup by production id. |
| `productionUid` | string | no | Filter the ticket lookup by production uid. |
| `ticketNumber` | string | no | Ticket number to look up. |

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

Through the native PassKit Event Tickets API, this operation is `GET /eventTickets/ticket/ticketNumber` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-by-ticket-number.md) for the provider-specific parameters and requirements.

