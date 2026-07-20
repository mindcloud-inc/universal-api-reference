# GrooveHQ: Update Ticket Group

Updates a ticket's assigned group in GrooveHQ.

```
PUT https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-ticket-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-ticket-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketNumber": "1001",
  "group": "Support"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-ticket-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketNumber": "1001",
    "group": "Support"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketNumber` | string | yes | Example: `1001`. |
| `group` | string | yes | Example: `Support`. |
| `skipNotifications` | boolean | no | Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `PUT /tickets/:ticketNumber/assigned_group` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket-group.md) for the provider-specific parameters and requirements.

