# Ticketbud: Check In Ticket

Checks in a ticket in Ticketbud.

```
PUT https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/check-in-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketbud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/check-in-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/check-in-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The Ticketbud event ID that owns the ticket. |
| `id` | string | yes | The Ticketbud ticket ID to check in. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Ticket check-in counters for the event. |
| `ticket` | object | The updated Ticketbud ticket after check-in. |

## Native endpoint

Through the native Ticketbud API, this operation is `PUT /events/:eventId/tickets/:id/check_in.json` (base URL `https://api.ticketbud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-in-ticket.md) for the provider-specific parameters and requirements.

