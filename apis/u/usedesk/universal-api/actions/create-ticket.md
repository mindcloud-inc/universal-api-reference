# Usedesk: Create Ticket

Creates a new ticket in Usedesk.

```
POST https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientEmail` | string | no | Client email when creating or attaching the ticket. |
| `clientName` | string | no | Client name when creating or attaching the ticket. |
| `priority` | string | no | Ticket priority: low, medium, urgent, or extreme. |
| `subject` | string | yes | Ticket subject. |
| `type` | string | no | Ticket type: question, task, problem, or incident. |
| `message` | string | yes | First ticket message. Supports HTML markup. |
| `clientId` | number | no | Client ID or the string new_client. |
| `channelId` | number | no | Channel ID in which the ticket will be created. |
| `status` | number | no | Ticket status ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "ticket_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `ticket_id` | number |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /create/ticket` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

