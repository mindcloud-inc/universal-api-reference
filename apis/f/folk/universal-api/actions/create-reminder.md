# folk: Create Reminder

Creates a new reminder in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "name": "Ava Chen",
  "recurrenceRule": "string",
  "visibility": "private"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "name": "Ava Chen",
    "recurrenceRule": "string",
    "visibility": "private"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes | The ID of the entity connected to the reminder. |
| `name` | string | yes | The name of the reminder. |
| `recurrenceRule` | string | yes | The reminder recurrence rule in the supported iCalendar subset. |
| `visibility` | string | yes | The reminder visibility. Defaulted to private in this action. Default: `private`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedUserId` | string | no | The first assigned user ID for a public reminder. |
| `assignedUserEmail` | string | no | The first assigned user email for a public reminder. |
| `assignedUser2Id` | string | no | The second assigned user ID for a public reminder. |
| `assignedUser2Email` | string | no | The second assigned user email for a public reminder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedUsers": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "entity": {},
      "id": "string",
      "lastTriggerTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextTriggerTime": "2026-05-07T12:00:00.000Z",
      "recurrenceRule": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedUsers` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `entity` | object |  |
| `id` | string |  |
| `lastTriggerTime` | date |  |
| `name` | string |  |
| `nextTriggerTime` | date |  |
| `recurrenceRule` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native folk API, this operation is `POST /v1/reminders` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reminder.md) for the provider-specific parameters and requirements.

