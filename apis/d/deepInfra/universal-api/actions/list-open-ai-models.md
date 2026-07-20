# Deep Infra: List OpenAI Models



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Optional model sorting key documented by DeepInfra. Example: `created`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "id": "string",
      "metadata": {
        "contextLength": 1,
        "description": "string",
        "maxTokens": 1,
        "pricing": {
          "cacheReadTokens": 1,
          "inputTokens": 1,
          "outputTokens": 1
        },
        "tags": [
          "string"
        ]
      },
      "object": "string",
      "ownedBy": "Ava Chen",
      "parent": "string",
      "root": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Model creation timestamp from the OpenAI-compatible response. |
| `id` | string | DeepInfra model identifier. |
| `metadata` | object | Optional model metadata. |
| `metadata.contextLength` | number | Maximum context length from model metadata. |
| `metadata.description` | string | Model description when metadata is available. |
| `metadata.maxTokens` | number | Maximum output token count from model metadata. |
| `metadata.pricing` | object | Pricing details for the model when available. |
| `metadata.pricing.cacheReadTokens` | number | Cached-token read price per million tokens when available. |
| `metadata.pricing.inputTokens` | number | Input token price per million tokens when available. |
| `metadata.pricing.outputTokens` | number | Output token price per million tokens when available. |
| `metadata.tags` | array<string> | Provider tags describing model capabilities. |
| `object` | string | OpenAI-compatible object type. |
| `ownedBy` | string | Model owner from the mapped DeepInfra response. |
| `parent` | string | Parent model when present. |
| `root` | string | Root model identifier. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/models` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-ai-models.md) for the provider-specific parameters and requirements.

