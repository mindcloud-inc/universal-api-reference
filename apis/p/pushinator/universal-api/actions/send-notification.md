# Pushinator: Send Notification

Creates a new notification in a Pushinator channel.

```
POST https://connect.mindcloud.co/v1/universal/pushinator/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushinator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushinator/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushinator/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | The Pushinator channel ID that will receive the notification. |
| `content` | string | yes | The notification text to send. |
| `acknowledgmentRequired` | boolean | no | Whether subscribers must acknowledge the notification. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string | Pushinator response message |
| `success` | boolean | Whether Pushinator accepted the notification request |

## Native endpoint

Through the native Pushinator API, this operation is `POST /notifications/send` (base URL `https://api.pushinator.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

