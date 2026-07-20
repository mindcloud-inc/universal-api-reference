# Tidio: Reply to Ticket [Plus plan]

Replies to a ticket in the Tidio workspace.

```
POST https://connect.mindcloud.co/v1/universal/tidio/latest/actions/reply-to-ticket-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/reply-to-ticket-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "authorType": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/reply-to-ticket-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "authorType": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The Tidio ticket ID. |
| `authorType` | string | yes | Reply author type. |
| `content` | string | yes | Reply message content. |
| `operatorId` | string | no | Operator UUID when the reply author type is operator. |
| `messageType` | string | no | Reply visibility type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Tidio API, this operation is `POST /tickets/{ticketId}/reply` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-ticket-plus-plan.md) for the provider-specific parameters and requirements.

