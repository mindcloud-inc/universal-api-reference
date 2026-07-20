# Vybit: Create Reminder



```
POST https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cron": "string",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cron": "string",
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cron` | string | yes | Cron expression for when the reminder should fire |
| `imageUrl` | string | no | Image URL for this reminder |
| `key` | string | yes | The unique key of the vybit. |
| `linkUrl` | string | no | Link URL for this reminder |
| `log` | string | no | Log content for this reminder |
| `message` | string | no | Notification message for this reminder |
| `timeZone` | string | no | IANA time zone identifier |
| `year` | number | no | Year for a one-time reminder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reminder": {},
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reminder` | object |  |
| `result` | number |  |

## Native endpoint

Through the native Vybit API, this operation is `POST /vybit/{{key}}/reminders` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reminder.md) for the provider-specific parameters and requirements.

