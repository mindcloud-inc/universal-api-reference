# Chatnode: Send Message



```
POST https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatnode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The Chatnode agent id associated with the trained agent model. |
| `chatSessionId` | string | no | Optional chat session id to continue an existing conversation. |
| `message` | string | yes | The message to send to your agent. |
| `streaming` | boolean | no | Whether to enable streaming responses. Defaults to false. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_session_id": "string",
      "docs": [
        "string"
      ],
      "id": "string",
      "message": "string",
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_session_id` | string | Conversation session identifier. |
| `docs` | array<string> | Referenced document identifiers returned by Chatnode. |
| `id` | string | Message identifier. |
| `message` | string | Assistant response text. |
| `urls` | array<string> | Referenced URLs returned by Chatnode. |

## Native endpoint

Through the native Chatnode API, this operation is `POST :botId` (base URL `https://api.public.chatnode.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

