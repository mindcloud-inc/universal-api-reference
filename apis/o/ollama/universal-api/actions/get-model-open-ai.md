# Ollama: Get Model (OpenAI Compatible)

Retrieves an OpenAI-compatible model from Ollama.

```
GET https://connect.mindcloud.co/v1/universal/ollama/latest/actions/get-model-open-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/get-model-open-ai?connectionId=$CONNECTION_ID&model=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ollama/latest/actions/get-model-open-ai?${params}`, {
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
| `model` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "id": "string",
      "object": "string",
      "ownedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `id` | string |  |
| `object` | string |  |
| `ownedBy` | string |  |

## Native endpoint

Through the native Ollama API, this operation is `GET /v1/models/:model` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-open-ai.md) for the provider-specific parameters and requirements.

