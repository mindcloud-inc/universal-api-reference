# Datalyse: Create Ticket

Creates a new ticket in Datalyse.

```
POST https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string",
  "ticketDescription": "string",
  "ticketName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string",
    "ticketDescription": "string",
    "ticketName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | no | Set to "unassigned" to assign this ticket to all agents, or provide a specific agent_id (optional) Default: `unassigned`. |
| `leadId` | string | yes | ID of the contact or company |
| `pipeline` | string | no | Pipeline ID (optional) |
| `status` | string | no | Status ID Default: `0`. |
| `ticketDescription` | string | yes | Description for the ticket |
| `ticketName` | string | yes | Name for the ticket |
| `ticketVisibleCabinet` | string | no | Visible in client cabinet (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/tickets/create.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

