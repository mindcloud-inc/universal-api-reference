# SuperOps IT: Update Ticket



```
PUT https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The SuperOps ticket ID to update. |
| `subject` | string | no | Optional new ticket subject. |
| `status` | string | no | Optional ticket status name. |
| `priority` | string | no | Optional ticket priority name. |
| `resolutionCode` | string | no | Optional ticket resolution code. |
| `requestType` | string | no | Optional ticket request type name. |
| `requesterUserId` | string | no | Optional requester user ID. |
| `technicianUserId` | string | no | Optional technician user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateTicket": {
        "createdTime": "2026-05-07T12:00:00.000Z",
        "displayId": "string",
        "requestType": "string",
        "site": {
          "id": "string",
          "name": "Ava Chen"
        },
        "sla": {
          "id": 1,
          "name": "Ava Chen"
        },
        "status": "string",
        "subject": "string",
        "ticketId": "string",
        "updatedTime": "2026-05-07T12:00:00.000Z",
        "worklogTimespent": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updateTicket.createdTime` | date |  |
| `updateTicket.displayId` | string |  |
| `updateTicket.requestType` | string |  |
| `updateTicket.site.id` | string |  |
| `updateTicket.site.name` | string |  |
| `updateTicket.sla.id` | number |  |
| `updateTicket.sla.name` | string |  |
| `updateTicket.status` | string |  |
| `updateTicket.subject` | string |  |
| `updateTicket.ticketId` | string |  |
| `updateTicket.updatedTime` | date |  |
| `updateTicket.worklogTimespent` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

