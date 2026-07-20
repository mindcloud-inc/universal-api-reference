# Amazing Marvin: Set Reminders

Sets one or more reminders in Amazing Marvin.

```
PUT https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/set-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/set-reminders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reminders[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/set-reminders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reminders[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reminders[]` | array<object> | yes | Array of reminder objects to create or update. |
| `reminders[].time` | number | no | Unix timestamp for the reminder. |
| `reminders[].offset` | number | no | Minutes ahead of time to remind; use -1 for the Marvin default. |
| `reminders[].reminderId` | string | no | Unique reminder identifier, usually a task ID or random ID. |
| `reminders[].type` | string | no | Reminder type code such as T, M, DT, DP, or t. |
| `reminders[].title` | string | no | Reminder title shown in the notification. |
| `reminders[].snooze` | number | no | Snooze duration in minutes. |
| `reminders[].autoSnooze` | boolean | no | Whether the reminder should auto-snooze. |
| `reminders[].canTrack` | boolean | no | Whether the reminder can start time tracking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /reminder/set` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-reminders.md) for the provider-specific parameters and requirements.

