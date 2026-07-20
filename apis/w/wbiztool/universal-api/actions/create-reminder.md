# Wbiztool: Create Reminder

Creates a recurring WhatsApp reminder in Wbiztool.

```
POST https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/create-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/create-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msgType": "string",
  "reminderName": "Ava Chen",
  "phone": "string",
  "message": "string",
  "cronExpression": "string",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/create-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msgType": "string",
    "reminderName": "Ava Chen",
    "phone": "string",
    "message": "string",
    "cronExpression": "string",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msgType` | string | yes | Reminder message type as numeric text: 0 text, 1 image, 2 file. |
| `reminderName` | string | yes | Friendly name for the reminder. |
| `phone` | string | yes | Recipient phone number, including country code. |
| `message` | string | yes | Reminder message text. |
| `cronExpression` | string | yes | Cron expression that defines when the reminder runs. |
| `timezone` | string | yes | Timezone used for the cron schedule. |
| `imageUrl` | string | no | Public image URL for image reminders. |
| `fileUrl` | string | no | Public file URL for file reminders. |
| `fileName` | string | no | Optional display name for file reminders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "reminderId": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `reminderId` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /reminder/create/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reminder.md) for the provider-specific parameters and requirements.

