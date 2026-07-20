# Omnara: Get Agent Session Messages



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-agent-session-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-agent-session-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-agent-session-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "messages": [
        {
          "canceledAt": "string",
          "createdAt": "string",
          "deliveredAt": "string",
          "deliveryMode": "string",
          "messageId": "string",
          "metadata": {},
          "payload": {
            "content": {},
            "metadata": {},
            "version": 1
          },
          "sender": {
            "id": "string",
            "kind": "string"
          },
          "sessionId": "string"
        }
      ],
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `messages` | array<object> |  |
| `messages[]` | object |  |
| `messages[].canceledAt` | string |  |
| `messages[].createdAt` | string |  |
| `messages[].deliveredAt` | string |  |
| `messages[].deliveryMode` | string |  |
| `messages[].messageId` | string |  |
| `messages[].metadata` | object |  |
| `messages[].payload` | object |  |
| `messages[].payload.content` | object |  |
| `messages[].payload.metadata` | object |  |
| `messages[].payload.version` | number |  |
| `messages[].sender` | object |  |
| `messages[].sender.id` | string |  |
| `messages[].sender.kind` | string |  |
| `messages[].sessionId` | string |  |
| `nextCursor` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/user-sessions/{userSessionId}/agent-sessions/{agentSessionId}/messages` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-session-messages.md) for the provider-specific parameters and requirements.

