# GrooveHQ: Create Message

Creates a new message in a GrooveHQ ticket.

```
POST https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketNumber": "1001",
  "body": "Following up on your request."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketNumber": "1001",
    "body": "Following up on your request."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketNumber` | string | yes | Example: `1001`. |
| `body` | string | yes | Example: `Following up on your request.`. |
| `author` | string | no | Example: `agent@example.com`. |
| `sentAt` | date | no | Example: `2026-04-14T10:00:00Z`. |
| `note` | boolean | no | Example: `false`. |
| `sendCopyToCustomer` | boolean | no | Example: `false`. |
| `skipUnreadTicket` | boolean | no | Example: `false`. |
| `skipNotifications` | boolean | no | Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `POST /tickets/:ticketNumber/messages` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

