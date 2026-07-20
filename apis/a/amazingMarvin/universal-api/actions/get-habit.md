# Amazing Marvin: Get Habit

Retrieves a habit and its history from Amazing Marvin.

```
GET https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-habit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-habit?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-habit?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Habit ID to retrieve. |

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

Through the native Amazing Marvin API, this operation is `GET /habit` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-habit.md) for the provider-specific parameters and requirements.

