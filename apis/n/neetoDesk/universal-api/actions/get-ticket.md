# NeetoDesk: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | string | yes | Identifier of the ticket. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoDesk API returns.

## Native endpoint

Through the native NeetoDesk API, this operation is `GET /tickets/:ticket_id` (base URL `https://{{credentials.workspaceSubdomain}}.neetodesk.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

