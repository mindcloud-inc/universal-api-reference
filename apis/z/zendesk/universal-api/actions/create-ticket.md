# Zendesk: Create Ticket

Creates a new ticket in Zendesk.

```
POST https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticket.comment.body": "Describe the issue in detail"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticket.comment.body": "Describe the issue in detail"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticket.comment.body` | string | yes | Initial ticket comment. Default: `MindCloud test ticket comment body.`. Example: `Describe the issue in detail`. |
| `ticket.subject` | string | no | Ticket subject line. Default: `MindCloud test ticket subject`. Example: `Issue summary`. |
| `ticket.priority` | string | no | Ticket priority (low, normal, high, urgent). One of: `0`, `1`, `2`, `3`. |
| `ticket.status` | string | no | Ticket status (new, open, pending, hold, solved, closed). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "groupId": 1,
      "id": 1,
      "isPublic": true,
      "organizationId": 1,
      "priority": "string",
      "requesterId": 1,
      "status": "string",
      "subject": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `isPublic` | boolean |  |
| `organizationId` | number |  |
| `priority` | string |  |
| `requesterId` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `tags[]` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Zendesk API, this operation is `POST /tickets.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

