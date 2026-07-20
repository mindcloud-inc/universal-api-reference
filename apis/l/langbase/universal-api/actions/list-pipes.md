# Langbase: List Pipes



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-pipes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-pipes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-pipes?${params}`, {
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
      "description": "string",
      "frequencyPenalty": 1,
      "json": true,
      "maxTokens": 1,
      "memory": [
        {}
      ],
      "messages": [
        {}
      ],
      "model": "string",
      "moderate": true,
      "name": "Ava Chen",
      "ownerLogin": "string",
      "parallelToolCalls": true,
      "presencePenalty": 1,
      "status": "string",
      "stop": [
        "string"
      ],
      "store": true,
      "stream": true,
      "temperature": 1,
      "toolChoice": "string",
      "tools": [
        {}
      ],
      "topP": 1,
      "variables": [
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
| `description` | string |  |
| `frequencyPenalty` | number |  |
| `json` | boolean |  |
| `maxTokens` | number |  |
| `memory` | array<object> |  |
| `messages` | array<object> |  |
| `model` | string |  |
| `moderate` | boolean |  |
| `name` | string |  |
| `ownerLogin` | string |  |
| `parallelToolCalls` | boolean |  |
| `presencePenalty` | number |  |
| `status` | string |  |
| `stop` | array<string> |  |
| `store` | boolean |  |
| `stream` | boolean |  |
| `temperature` | number |  |
| `toolChoice` | string |  |
| `tools` | array<object> |  |
| `topP` | number |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native Langbase API, this operation is `GET v1/pipes` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipes.md) for the provider-specific parameters and requirements.

