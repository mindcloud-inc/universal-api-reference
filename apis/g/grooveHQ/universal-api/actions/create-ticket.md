# GrooveHQ: Create Ticket

Creates a new ticket in GrooveHQ.

```
POST https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "How can we help?",
  "from": "agent@example.com",
  "to": "customer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "How can we help?",
    "from": "agent@example.com",
    "to": "customer@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | Example: `How can we help?`. |
| `from` | string | yes | Example: `agent@example.com`. |
| `to` | string | yes | Example: `customer@example.com`. |
| `mailbox` | string | no | Example: `support@example.com`. |
| `assignedGroup` | string | no | Example: `Support`. |
| `assignee` | string | no | Example: `agent@example.com`. |
| `note` | boolean | no | Example: `false`. |
| `sendCopyToCustomer` | boolean | no | Example: `false`. |
| `state` | string | no | Example: `unread`. |
| `subject` | string | no | Example: `New support request`. |
| `tags[]` | array<string> | no | Accepts multiple values as an array. Example: `billing, urgent`. |
| `tags[]` | array<string> | no | Accepts multiple values as an array. Example: `billing, urgent`. |
| `starred` | boolean | no | Example: `false`. |
| `skipNotifications` | boolean | no | Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `POST /tickets` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

