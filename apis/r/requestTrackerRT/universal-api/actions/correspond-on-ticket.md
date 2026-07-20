# Request Tracker (RT): Correspond on Ticket

Adds a reply to a ticket in Request Tracker.

```
PUT https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/correspond-on-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/correspond-on-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "contentType": "text/plain",
  "ticketId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/correspond-on-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "contentType": "text/plain",
    "ticketId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Reply body to add to the ticket. |
| `contentType` | string | yes | Content type for the reply body. Default: `text/plain`. |
| `subject` | string | no | Optional subject for the correspondence. |
| `ticketId` | string | yes | The numeric RT ticket ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Request Tracker (RT) API returns.

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `POST ticket/:ticketId/correspond` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/correspond-on-ticket.md) for the provider-specific parameters and requirements.

