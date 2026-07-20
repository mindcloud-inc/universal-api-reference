# Wrangle: Update Ticket



```
PUT https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "ticket_uuid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/update-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "ticket_uuid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The Wrangle ticket ID. Example: `ticket_uuid`. |
| `description` | string | no | The ticket description. |
| `name` | string | no | The updated ticket name. |
| `priority` | list | no | Updated ticket priority. One of: `0`, `1`, `2`, `3`. |
| `status` | list | no | Updated ticket status. One of: `0`, `1`, `2`, `3`, `4`. |
| `tags[]` | array<string> | no | Updated ticket tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | string | no | The Slack user ID of the ticket assignee. Use null to unassign. |
| `csatScore` | list | no | The customer satisfaction score for the ticket. One of: `0`, `1`, `2`, `3`, `4`. |
| `followers[]` | array<object> | no | Follower objects to add to the ticket. |
| `formFieldValues[]` | array<object> | no | Updated form field values for the ticket. |
| `inboxId` | string | no | Move the ticket to a new inbox. |

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

Through the native Wrangle API, this operation is `PUT /tickets/:ticketId` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

