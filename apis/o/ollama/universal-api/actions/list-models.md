# Ollama: List Models

Retrieves available models from Ollama.

```
GET https://connect.mindcloud.co/v1/universal/ollama/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ollama/latest/actions/list-models?${params}`, {
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
      "models": [
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
| `models` | array<object> |  |

## Native endpoint

Through the native Ollama API, this operation is `GET /api/tags` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

