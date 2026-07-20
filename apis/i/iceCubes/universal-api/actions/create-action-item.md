# IceCubes: Create Action Item



```
POST https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/create-action-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/create-action-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/create-action-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meetingId` | string | yes | The meeting ID to attach the action item to. |
| `text` | string | yes | The action item text. |
| `assigneeEmail` | string | no | Assign the action item to an email address. |
| `dueDate` | date | no | Optional due date in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeEmail": "ava@example.com",
      "completed": true,
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "meetingId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeEmail` | string | Assigned email address. |
| `completed` | boolean | Completion status. |
| `dueDate` | date | Due date. |
| `id` | string | Action item ID. |
| `meetingId` | string | Meeting ID the action item belongs to. |
| `text` | string | Action item text. |

## Native endpoint

Through the native IceCubes API, this operation is `POST /action-items` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action-item.md) for the provider-specific parameters and requirements.

