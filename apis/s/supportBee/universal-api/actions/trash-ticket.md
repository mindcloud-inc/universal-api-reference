# SupportBee: Trash Ticket

Moves a SupportBee ticket to trash.

```
PUT https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/trash-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/trash-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/trash-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | SupportBee ticket ID. |

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

Through the native SupportBee API, this operation is `POST /tickets/:id/trash` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trash-ticket.md) for the provider-specific parameters and requirements.

