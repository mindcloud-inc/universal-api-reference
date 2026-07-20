# SuperOps IT: Create Ticket



```
POST https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "siteId": "string",
  "requestType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "siteId": "string",
    "requestType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | The subject of the ticket. |
| `description` | string | no | The description of the ticket. |
| `siteId` | string | yes | The site ID associated with the ticket. |
| `requestType` | string | yes | The ticket request type name. |
| `requesterUserId` | string | no | Optional requester user ID. |
| `technicianUserId` | string | no | Optional technician user ID. |
| `status` | string | no | Optional ticket status name. |
| `priority` | string | no | Optional ticket priority name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTicket": {
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
| `createTicket.createdTime` | date |  |
| `createTicket.displayId` | string |  |
| `createTicket.requestType` | string |  |
| `createTicket.site.id` | string |  |
| `createTicket.site.name` | string |  |
| `createTicket.sla.id` | number |  |
| `createTicket.sla.name` | string |  |
| `createTicket.status` | string |  |
| `createTicket.subject` | string |  |
| `createTicket.ticketId` | string |  |
| `createTicket.updatedTime` | date |  |
| `createTicket.worklogTimespent` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

