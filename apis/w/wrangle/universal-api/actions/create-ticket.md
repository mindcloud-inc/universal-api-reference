# Wrangle: Create Ticket



```
POST https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Quarterly access request",
  "inboxId": "inbox_uuid",
  "requesterId": "U12345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Quarterly access request",
    "inboxId": "inbox_uuid",
    "requesterId": "U12345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the ticket. Example: `Quarterly access request`. |
| `inboxId` | string | yes | The Wrangle inbox ID that will own the ticket. Example: `inbox_uuid`. |
| `requesterId` | string | yes | The Slack user ID of the ticket requester. Example: `U12345678`. |
| `description` | string | no | The ticket description. |
| `priority` | list | no | Ticket priority. One of: `0`, `1`, `2`, `3`. |
| `tags[]` | array<string> | no | Tags to assign to the ticket. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formFieldValues[]` | array<object> | no | Form field values for the ticket intake form. |

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

Through the native Wrangle API, this operation is `POST /tickets` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

