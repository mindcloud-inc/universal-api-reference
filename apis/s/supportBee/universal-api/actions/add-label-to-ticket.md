# SupportBee: Add Label to Ticket

Adds a label to a SupportBee ticket.

```
PUT https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/add-label-to-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/add-label-to-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1,
  "labelName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/add-label-to-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1,
    "labelName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | number | yes | SupportBee ticket ID. |
| `labelName` | string | yes | Label name to attach to the ticket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": {
        "id": 1,
        "label": "string",
        "ticket": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | object |  |
| `label.id` | number |  |
| `label.label` | string |  |
| `label.ticket` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `POST /tickets/:ticket_id/labels/:label_name` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-label-to-ticket.md) for the provider-specific parameters and requirements.

