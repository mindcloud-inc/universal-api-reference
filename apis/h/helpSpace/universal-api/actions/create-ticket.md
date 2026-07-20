# HelpSpace: Create Ticket

Creates a new ticket in HelpSpace.

```
POST https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native HelpSpace API, this operation is `POST /tickets` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

