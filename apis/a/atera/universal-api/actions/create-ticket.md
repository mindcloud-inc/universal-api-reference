# Atera: Create ticket

Creates a ticket in Atera.

```
POST https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "ticketTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "ticketTitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes | Ticket description. |
| `endUserEmail` | string | no | New end user email. |
| `endUserFirstName` | string | no | New end user first name. |
| `endUserId` | number | no | Existing end user contact ID. |
| `endUserLastName` | string | no | New end user last name. |
| `endUserPhone` | string | no | New end user phone. |
| `technicianContactId` | number | no | Technician contact ID. |
| `technicianEmail` | string | no | Technician email. |
| `ticketImpact` | string | no | Ticket impact. |
| `ticketPriority` | string | no | Ticket priority. |
| `ticketStatus` | string | no | Ticket status. |
| `ticketTitle` | string | yes | Ticket title. |
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

Through the native Atera API, this operation is `POST /api/v3/tickets` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

