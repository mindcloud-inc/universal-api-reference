# Deep Infra: List OpenRouter Models



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-router-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-router-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-router-models?${params}`, {
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
      "architecture": {},
      "context_length": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "pricing": {},
      "top_provider": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `architecture` | object | Model architecture metadata. |
| `context_length` | number | Maximum context length. |
| `description` | string | Model description. |
| `id` | string | OpenRouter-compatible model identifier. |
| `name` | string | Model display name. |
| `pricing` | object | OpenRouter-style pricing metadata. |
| `top_provider` | object | Top provider metadata. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /openrouter/models` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-router-models.md) for the provider-specific parameters and requirements.

