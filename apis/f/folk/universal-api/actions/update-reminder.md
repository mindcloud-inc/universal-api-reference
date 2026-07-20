# folk: Update Reminder

Updates an existing reminder in folk.

```
PUT https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reminderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reminderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reminderId` | string | yes | The ID of the reminder to update. |
| `name` | string | no | The updated name of the reminder. |
| `recurrenceRule` | string | no | The updated reminder recurrence rule in the supported iCalendar subset. |
| `visibility` | string | no | The reminder visibility. Set public or private. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedUserId` | string | no | The first assigned user ID when updating a public reminder. |
| `assignedUserEmail` | string | no | The first assigned user email when updating a public reminder. |
| `assignedUser2Id` | string | no | The second assigned user ID when updating a public reminder. |
| `assignedUser2Email` | string | no | The second assigned user email when updating a public reminder. |

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

Through the native folk API, this operation is `PATCH /v1/reminders/:reminderId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reminder.md) for the provider-specific parameters and requirements.

