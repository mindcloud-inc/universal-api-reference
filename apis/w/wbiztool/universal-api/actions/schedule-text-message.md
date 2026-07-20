# Wbiztool: Schedule Text Message

Creates a scheduled WhatsApp text message in Wbiztool.

```
POST https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/schedule-text-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/schedule-text-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "scheduledDate": "string",
  "scheduledTime": "string",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/schedule-text-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "scheduledDate": "string",
    "scheduledTime": "string",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | no | Recipient phone number with or without country code. |
| `groupName` | string | no | WhatsApp group name to message instead of a direct phone number. |
| `countryCode` | string | no | Country code for the recipient phone number. |
| `message` | string | yes | Message text to schedule. |
| `scheduledDate` | string | yes | Date to send the message in dd/mm/yyyy format. |
| `scheduledTime` | string | yes | Time to send the message in HH:MM format. |
| `timezone` | string | yes | Timezone used for the scheduled date and time. |
| `webhookUrl` | string | no | Optional webhook URL to receive message events. |
| `expireAfterSeconds` | number | no | Expire the message if it has not been sent before this many seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "msgId": 1,
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
| `msgId` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /schedule_msg/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-text-message.md) for the provider-specific parameters and requirements.

