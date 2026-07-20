# Zoho Desk: Move Ticket



```
PUT https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/move-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/move-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "departmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/move-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "departmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The Zoho Desk ticket ID. |
| `departmentId` | string | yes | Target department for the ticket move. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Desk API returns.

## Native endpoint

Through the native Zoho Desk API, this operation is `POST /tickets/[:ticketId]/move` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-ticket.md) for the provider-specific parameters and requirements.

