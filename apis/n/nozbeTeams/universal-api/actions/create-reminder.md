# Nozbe Teams: Create Reminder

Creates a new reminder in Nozbe Teams.

```
POST https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "remindAt": 1,
  "isRelative": true,
  "isAllDay": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "remindAt": 1,
    "isRelative": true,
    "isAllDay": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The task that will receive the reminder. |
| `remindAt` | number | yes | Unix timestamp in milliseconds for when to remind. |
| `isRelative` | boolean | yes | Whether the reminder is relative to the task date. |
| `isAllDay` | boolean | yes | Whether the reminder lasts all day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isAllDay": true,
      "isRelative": true,
      "remindAt": 1,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `isRelative` | boolean |  |
| `remindAt` | number |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `POST /reminders` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reminder.md) for the provider-specific parameters and requirements.

