# GrooveHQ: Update Ticket Assignee

Updates a ticket's assignee in GrooveHQ.

```
PUT https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-ticket-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-ticket-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketNumber": "1001",
  "assignee": "agent@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-ticket-assignee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketNumber": "1001",
    "assignee": "agent@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketNumber` | string | yes | Example: `1001`. |
| `assignee` | string | yes | Example: `agent@example.com`. |
| `skipNotifications` | boolean | no | Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `PUT /tickets/:ticketNumber/assignee` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket-assignee.md) for the provider-specific parameters and requirements.

