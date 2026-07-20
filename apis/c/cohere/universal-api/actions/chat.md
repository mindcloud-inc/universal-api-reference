# Cohere: Chat

Generates a chat response in Cohere.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/chat?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/chat?${params}`, {
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
      "chatHistory": [
        {}
      ],
      "citations": [
        {}
      ],
      "documents": [
        {}
      ],
      "finishReason": "string",
      "generationId": "string",
      "meta": {},
      "responseId": "string",
      "searchQueries": [
        {}
      ],
      "searchResults": [
        {}
      ],
      "text": "string",
      "toolCalls": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatHistory` | array<object> |  |
| `citations` | array<object> |  |
| `documents` | array<object> |  |
| `finishReason` | string |  |
| `generationId` | string |  |
| `meta` | object |  |
| `responseId` | string |  |
| `searchQueries` | array<object> |  |
| `searchResults` | array<object> |  |
| `text` | string |  |
| `toolCalls` | array<object> |  |

## Native endpoint

Through the native Cohere API, this operation is `POST /v1/chat` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat.md) for the provider-specific parameters and requirements.

