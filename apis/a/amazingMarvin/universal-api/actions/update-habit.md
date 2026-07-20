# Amazing Marvin: Update Habit

Updates habit history in Amazing Marvin.

```
PUT https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/update-habit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/update-habit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "habitId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/update-habit', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "habitId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `habitId` | string | yes | Habit identifier to update. |
| `time` | number | no | Timestamp to record for the habit update. |
| `value` | number | no | Numeric value to record for the habit update. |
| `undo` | boolean | no | Set to true to undo the last habit recording. |
| `history[]` | array<number> | no | Flat array used to rewrite the habit history. |
| `updateDB` | boolean | no | Set to true to update the Cloudant habit document as well. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "habitId": "string",
      "history": [
        1
      ],
      "nextReminder": 1,
      "nextReminderAt": "2026-05-07T12:00:00.000Z",
      "nextShareAt": "2026-05-07T12:00:00.000Z",
      "period": 1,
      "reminders": {},
      "shareEmails": {},
      "time": "string",
      "timeZoneOffset": 1,
      "userId": 1,
      "weekDay": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `habitId` | string |  |
| `history[]` | number |  |
| `nextReminder` | number |  |
| `nextReminderAt` | date |  |
| `nextShareAt` | date |  |
| `period` | number |  |
| `reminders` | object |  |
| `shareEmails` | object |  |
| `time` | string |  |
| `timeZoneOffset` | number |  |
| `userId` | number |  |
| `weekDay` | number |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /updateHabit` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-habit.md) for the provider-specific parameters and requirements.

