# Push by Techulus: Send Notification



```
POST https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Push by Techulus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Test",
  "body": "Test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Test",
    "body": "Test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Notification title. Default: `Test`. |
| `body` | string | yes | Notification body text. Default: `Test`. |
| `sound` | string | no | Optional notification sound. Valid values include default, arcade, correct, fail, harp, reveal, bubble, doorbell, flute, money, scifi, clear, elevator, guitar, and pop. |
| `channel` | string | no | Optional notification channel. Defaults to feed. Default: `feed`. |
| `link` | string | no | Optional notification link URL. |
| `image` | string | no | Optional notification image URL. |
| `timeSensitive` | boolean | no | Deliver immediately on iOS even during Do Not Disturb. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responses` | array<object> | Provider response collection returned by Push. |
| `success` | boolean | Whether the Push API accepted the notification request. |

## Native endpoint

Through the native Push by Techulus API, this operation is `POST /api/v1/notify` (base URL `https://push.techulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

