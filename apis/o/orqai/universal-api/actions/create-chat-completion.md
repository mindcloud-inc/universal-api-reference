# Orq.ai: Create Chat Completion

Creates a chat completion in Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-chat-completion?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-chat-completion?${params}`, {
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
      "choices": [
        {
          "index": 1,
          "message": {
            "content": "string",
            "role": "string"
          }
        }
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices[].index` | number |  |
| `choices[].message.content` | string |  |
| `choices[].message.role` | string |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/router/chat/completions` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

