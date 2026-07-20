# Zulip: Send Message

Creates a new message in Zulip.

```
POST https://connect.mindcloud.co/v1/universal/zulip/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "to": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zulip/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "to": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The Markdown message content to send. |
| `to` | string | yes | The target channel name, user email, or recipient list, depending on type. |
| `topic` | string | no | The topic for stream messages. |
| `type` | string | yes | The Zulip message type, such as stream or private. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `msg` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `POST /messages` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

