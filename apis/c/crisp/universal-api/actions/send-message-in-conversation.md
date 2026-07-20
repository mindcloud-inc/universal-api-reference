# Crisp: Send Message In Conversation

Sends a message in a Crisp conversation.

```
POST https://connect.mindcloud.co/v1/universal/crisp/latest/actions/send-message-in-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/send-message-in-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string",
  "sessionId": "string",
  "type": "text",
  "from": "user",
  "origin": "chat",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crisp/latest/actions/send-message-in-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string",
    "sessionId": "string",
    "type": "text",
    "from": "user",
    "origin": "chat",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteId` | string | yes | The website identifier |
| `sessionId` | string | yes | The conversation session identifier |
| `type` | string | yes | Message type Default: `text`. |
| `from` | list | yes | Message sender One of: `operator`, `user`. Default: `user`. |
| `origin` | list | yes | Message origin One of: `chat`, `email`, `urn:*`. Default: `chat`. |
| `content` | string | yes | Message content |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fingerprint": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fingerprint` | number |  |

## Native endpoint

Through the native Crisp API, this operation is `POST /website/:website_id/conversation/:session_id/message` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-in-conversation.md) for the provider-specific parameters and requirements.

