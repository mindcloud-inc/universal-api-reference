# SuperOps IT: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | string | yes | The SuperOps ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getTicket": {
        "createdTime": "2026-05-07T12:00:00.000Z",
        "displayId": "string",
        "firstResponseViolated": true,
        "requester": {
          "name": "Ava Chen",
          "userId": "string"
        },
        "requestType": "string",
        "resolutionViolated": true,
        "site": {
          "id": "string",
          "name": "Ava Chen"
        },
        "source": "string",
        "status": "string",
        "subject": "string",
        "technician": {
          "name": "Ava Chen",
          "userId": "string"
        },
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
| `getTicket.createdTime` | date |  |
| `getTicket.displayId` | string |  |
| `getTicket.firstResponseViolated` | boolean |  |
| `getTicket.requester.name` | string |  |
| `getTicket.requester.userId` | string |  |
| `getTicket.requestType` | string |  |
| `getTicket.resolutionViolated` | boolean |  |
| `getTicket.site.id` | string |  |
| `getTicket.site.name` | string |  |
| `getTicket.source` | string |  |
| `getTicket.status` | string |  |
| `getTicket.subject` | string |  |
| `getTicket.technician.name` | string |  |
| `getTicket.technician.userId` | string |  |
| `getTicket.ticketId` | string |  |
| `getTicket.updatedTime` | date |  |
| `getTicket.worklogTimespent` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

