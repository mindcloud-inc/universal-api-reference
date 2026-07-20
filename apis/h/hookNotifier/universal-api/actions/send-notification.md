# Hook.Notifier: Send Notification

Sends a custom notification through Hook.Notifier.

```
POST https://connect.mindcloud.co/v1/universal/hookNotifier/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hook.Notifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hookNotifier/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookNotifier/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | string | yes | Title of the notification. |
| `body` | string | yes | Content of the notification. |
| `tags` | string | no | Comma-separated tags for filtering, for example general,ops. |
| `color` | string | no | Hex color for the notification, for example #FFC107. |
| `image` | string | no | Image URL shown inside the notification. |
| `sound` | boolean | no | Activate the notification sound on phone. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `redirectUrl` | string | no | URL opened when the notification is clicked. Premium feature. |
| `sendToTeam` | boolean | no | Send the notification to you and your team. Premium feature. |
| `preventData` | boolean | no | Disable data storage in the notification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Hook.Notifier success status. |

## Native endpoint

Through the native Hook.Notifier API, this operation is `POST /` (base URL `https://hooknotifier.com/{{credentials.identifier}}/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

