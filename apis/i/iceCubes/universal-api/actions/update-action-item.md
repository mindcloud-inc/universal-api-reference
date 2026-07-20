# IceCubes: Update Action Item



```
PUT https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/update-action-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/update-action-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionItemId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/update-action-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionItemId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionItemId` | string | yes | The action item ID to update. |
| `completed` | boolean | no | Mark the action item complete or incomplete. |
| `text` | string | no | Updated action item text. |

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

Through the native IceCubes API, this operation is `PATCH /action-items/:id` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action-item.md) for the provider-specific parameters and requirements.

