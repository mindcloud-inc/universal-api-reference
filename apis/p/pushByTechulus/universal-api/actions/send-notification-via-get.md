# Push by Techulus: Send Notification via GET



```
POST https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/send-notification-via-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Push by Techulus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/send-notification-via-get" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/send-notification-via-get', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Notification title. |
| `body` | string | yes | Notification body text. |
| `sound` | string | no | Optional notification sound. |
| `channel` | string | no | Optional notification channel. Default: `feed`. |
| `link` | string | no | Optional URL opened by the notification. |
| `image` | string | no | Optional image URL. |
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
| `success` | boolean | Whether the Push API accepted the GET notification request. |

## Native endpoint

Through the native Push by Techulus API, this operation is `GET /api/v1/notify/:apiKey` (base URL `https://push.techulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification-via-get.md) for the provider-specific parameters and requirements.

