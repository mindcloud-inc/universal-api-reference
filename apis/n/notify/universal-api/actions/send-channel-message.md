# Notify: Send Channel Message

Creates a new message in a Notify channel.

```
POST https://connect.mindcloud.co/v1/universal/notify/latest/actions/send-channel-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notify/latest/actions/send-channel-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notify/latest/actions/send-channel-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | no | Optional URL to open when the notification is clicked. |
| `channelId` | string | no | A Notify channel token or ID. |
| `message` | string | no | The notification text to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | The raw response bytes. Notify returns the UTF-8 bytes for `ok` on success. |
| `type` | string | The runtime wrapper type for the raw text response. |

## Native endpoint

Through the native Notify API, this operation is `POST /:channelId` (base URL `https://notify.run`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-channel-message.md) for the provider-specific parameters and requirements.

