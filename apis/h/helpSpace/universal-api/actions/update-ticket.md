# HelpSpace: Update Ticket

Updates an existing ticket in HelpSpace.

```
PUT https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | HelpSpace ticket identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "channel": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {},
      "customFields": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "fromContact": {},
      "id": 1,
      "lastContact": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "tags": [
        "string"
      ],
      "team": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `channel` | object |  |
| `createdAt` | date |  |
| `creator` | object |  |
| `customFields` | object |  |
| `deletedAt` | date |  |
| `fromContact` | object |  |
| `id` | number |  |
| `lastContact` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `tags` | array |  |
| `team` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HelpSpace API, this operation is `PATCH /tickets/{id}` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

