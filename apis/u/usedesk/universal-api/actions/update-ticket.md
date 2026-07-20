# Usedesk: Update Ticket

Updates an existing ticket in Usedesk.

```
PUT https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/update-ticket', {
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
| `priority` | string | no | Ticket priority: low, medium, urgent, or extreme. |
| `silent` | string | no | Disable the automatic status change when true or 1. |
| `subject` | string | no | Ticket subject. |
| `tag` | string | no | Tags separated by comma and space. |
| `ticketId` | number | yes | Ticket ID. |
| `type` | string | no | Ticket type: question, task, problem, or incident. |
| `clientId` | number | no | Client ID. |
| `groupId` | number | no | Group ID. |
| `assigneeId` | number | no | Assignee user ID. |
| `userId` | number | no | User ID on whose behalf the changes will be made. |
| `status` | number | no | Ticket status ID. |

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
| `status` | string |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /update/ticket` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

