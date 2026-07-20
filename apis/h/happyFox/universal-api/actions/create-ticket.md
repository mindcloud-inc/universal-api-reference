# HappyFox: Create Ticket

Creates a new ticket in HappyFox.

```
POST https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "subject": "string",
  "text": "string",
  "category": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "subject": "string",
    "text": "string",
    "category": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Requester name. |
| `email` | string | yes | Requester email address. |
| `subject` | string | yes | Ticket subject. |
| `text` | string | yes | Ticket body in plain text. |
| `category` | number | yes | HappyFox category ID for the ticket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {},
      "attachmentsCount": 1,
      "category": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "displayId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "firstMessage": "string",
      "id": 1,
      "lastStaffReplyAt": "2026-05-07T12:00:00.000Z",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "lastUserReplyAt": "2026-05-07T12:00:00.000Z",
      "messagesCount": 1,
      "priority": {},
      "slaBreaches": 1,
      "source": "string",
      "status": {},
      "subject": "string",
      "subscribers": [
        {}
      ],
      "tags": "string",
      "timeSpent": 1,
      "unresponded": true,
      "updates": [
        {}
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object | Assigned staff member, when present. |
| `attachmentsCount` | number | Number of ticket attachments. |
| `category` | object | Ticket category object. |
| `createdAt` | date | Ticket creation timestamp. |
| `customFields` | array<object> | Ticket custom field values. |
| `displayId` | string | Human-readable HappyFox ticket display ID. |
| `dueDate` | date | Ticket due date, when set. |
| `firstMessage` | string | Original ticket message body. |
| `id` | number | Internal HappyFox ticket ID. |
| `lastStaffReplyAt` | date | Most recent staff reply timestamp. |
| `lastUpdatedAt` | date | Last updated timestamp. |
| `lastUserReplyAt` | date | Most recent end-user reply timestamp. |
| `messagesCount` | number | Number of ticket messages. |
| `priority` | object | Ticket priority object. |
| `slaBreaches` | number | Number of SLA breaches. |
| `source` | string | Ticket source identifier. |
| `status` | object | Ticket status object. |
| `subject` | string | Ticket subject line. |
| `subscribers` | array<object> | Ticket subscribers. |
| `tags` | string | Comma-delimited ticket tags. |
| `timeSpent` | number | Tracked time spent on the ticket. |
| `unresponded` | boolean | Whether the ticket is awaiting response. |
| `updates` | array<object> | Ticket update history. |
| `user` | object | Primary contact attached to the ticket. |

## Native endpoint

Through the native HappyFox API, this operation is `POST /tickets/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

