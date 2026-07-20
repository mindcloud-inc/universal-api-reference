# PushAlert: Send Notification



```
POST https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "message": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "message": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action1` | string | no | JSON string with title and url for the first CTA button. |
| `action1Attr` | string | no | JSON string with title and url template for the first CTA button. |
| `action2` | string | no | JSON string with title and url for the second CTA button. |
| `action2Attr` | string | no | JSON string with title and url template for the second CTA button. |
| `attributes` | string | no | Single JSON object string used to target subscribers by custom attribute. |
| `audienceId` | string | no | Audience Creator ID for precise targeting. |
| `expireTime` | string | no | Notification expiry time in seconds. |
| `icon` | string | no | HTTPS icon URL for the notification. |
| `largeImage` | string | no | HTTPS hero image URL for the notification. |
| `messageAttr` | string | no | Notification message template using subscriber attributes. |
| `scheduleTime` | string | no | Unix timestamp for scheduled delivery. |
| `subscriber` | string | no | Single subscriber ID to target. |
| `subscribers` | string | no | JSON array string of subscriber IDs to target. |
| `timezoneSchedule` | string | no | ISO datetime for timezone-aware scheduling. |
| `title` | string | yes | Notification title. |
| `titleAttr` | string | no | Notification title template using subscriber attributes. |
| `urlAttr` | string | no | Destination URL template using subscriber attributes. |
| `message` | string | yes | Notification message body. |
| `url` | string | yes | Destination URL when the notification is clicked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | ID of the scheduled or sent notification. |
| `success` | boolean | Whether the notification request succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `POST /rest/v2/web-push/send` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

