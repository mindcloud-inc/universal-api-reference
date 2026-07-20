# Atera: Update ticket

Updates an existing ticket in Atera.

```
PUT https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `technicianContactId` | number | no | Technician contact ID. |
| `technicianEmail` | string | no | Technician email. |
| `ticketId` | number | yes | System ticket ID. |
| `ticketImpact` | string | no | Ticket impact. |
| `ticketPriority` | string | no | Ticket priority. |
| `ticketStatus` | string | no | Ticket status. |
| `ticketTitle` | string | no | Ticket title. |
| `ticketType` | string | no | Ticket type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionID` | string |  |

## Native endpoint

Through the native Atera API, this operation is `PUT /api/v3/tickets/:ticketId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

