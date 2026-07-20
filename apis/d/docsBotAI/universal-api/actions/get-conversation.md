# DocsBot AI: Get Conversation

Retrieves a conversation from DocsBot AI.

```
GET https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/get-conversation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/get-conversation?${params}`, {
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
      "alias": "string",
      "answered": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "escalated": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "history": [
        {}
      ],
      "id": "string",
      "ip": "string",
      "metadata": {},
      "model": "string",
      "resolved": "string",
      "sentiment": 1,
      "summary": "string",
      "ticketContent": "string",
      "ticketSubject": "string",
      "title": "string",
      "truncated": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `answered` | boolean |  |
| `createdAt` | date |  |
| `escalated` | string |  |
| `expiresAt` | date |  |
| `history` | array<object> |  |
| `id` | string |  |
| `ip` | string |  |
| `metadata` | object |  |
| `model` | string |  |
| `resolved` | string |  |
| `sentiment` | number |  |
| `summary` | string |  |
| `ticketContent` | string |  |
| `ticketSubject` | string |  |
| `title` | string |  |
| `truncated` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `GET /teams/:teamId/bots/:botId/conversations/:conversationId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

