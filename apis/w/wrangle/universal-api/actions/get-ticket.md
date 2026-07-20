# Wrangle: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=ticket_uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "ticket_uuid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | string | yes | The Wrangle ticket ID. Example: `ticket_uuid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "ticket": {
        "assigneeId": {},
        "createdAt": "string",
        "creatorId": "string",
        "csatReason": {},
        "csatScore": {},
        "description": "string",
        "id": "string",
        "inboxId": "string",
        "name": "Ava Chen",
        "priority": "string",
        "requesterId": "string",
        "slackMessageChannel": "string",
        "slackMessageTs": "string",
        "slackOriginalMessage": {},
        "slackParentMessageTs": "string",
        "slackPermalinkUrl": "https://example.com",
        "status": "string",
        "updatedAt": "string",
        "workspaceId": "string",
        "workspaceTicketNumber": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `ticket.assigneeId` | object |  |
| `ticket.createdAt` | string |  |
| `ticket.creatorId` | string |  |
| `ticket.csatReason` | object |  |
| `ticket.csatScore` | object |  |
| `ticket.description` | string |  |
| `ticket.id` | string |  |
| `ticket.inboxId` | string |  |
| `ticket.name` | string |  |
| `ticket.priority` | string |  |
| `ticket.requesterId` | string |  |
| `ticket.slackMessageChannel` | string |  |
| `ticket.slackMessageTs` | string |  |
| `ticket.slackOriginalMessage` | object |  |
| `ticket.slackParentMessageTs` | string |  |
| `ticket.slackPermalinkUrl` | string |  |
| `ticket.status` | string |  |
| `ticket.updatedAt` | string |  |
| `ticket.workspaceId` | string |  |
| `ticket.workspaceTicketNumber` | number |  |

## Native endpoint

Through the native Wrangle API, this operation is `GET /tickets/:ticketId` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

