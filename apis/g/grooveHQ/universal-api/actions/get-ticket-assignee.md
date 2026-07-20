# GrooveHQ: Get Ticket Assignee

Retrieves a ticket's assignee from GrooveHQ.

```
GET https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-ticket-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-ticket-assignee?connectionId=$CONNECTION_ID&ticketNumber=1001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketNumber": "1001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-ticket-assignee?${params}`, {
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
| `ticketNumber` | string | yes | Example: `1001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `GET /tickets/:ticketNumber/assignee` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-assignee.md) for the provider-specific parameters and requirements.

