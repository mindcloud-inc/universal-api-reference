# SMS.to: Schedule Sending Messages

Schedules personalized SMS messages for later delivery in SMS.to.

```
POST https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/schedule-sending-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/schedule-sending-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].message": "string",
  "messages[].to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/schedule-sending-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].message": "string",
    "messages[].to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes | Array of message objects with recipient phone numbers. |
| `messages[].message` | string | yes | Each message text. |
| `messages[].to` | string | yes | Recipient phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderId` | string | no | The displayed value of who sent the message. |
| `scheduledFor` | date | no | Date and time when the messages will be sent. Format: YYYY-MM-DD HH:MM:SS. |
| `timezone` | string | no | TZ database name. |
| `bypassOptout` | boolean | no | True will bypass opt-outs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SMS.to API, this operation is `POST /sms/send` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-sending-messages.md) for the provider-specific parameters and requirements.

