# NVIDIA: Create Chat Completion (google/gemma-7b)

Creates a chat completion in NVIDIA using google/gemma-7b.

```
POST https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/create-chat-completion-google-gemma-7b
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NVIDIA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/create-chat-completion-google-gemma-7b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/create-chat-completion-google-gemma-7b', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native NVIDIA API, this operation is `POST /v1/chat/completions` (base URL `https://integrate.api.nvidia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion-google-gemma-7b.md) for the provider-specific parameters and requirements.

