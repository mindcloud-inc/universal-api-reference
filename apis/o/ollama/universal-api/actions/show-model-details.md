# Ollama: Show Model Details

Retrieves model details from Ollama.

```
GET https://connect.mindcloud.co/v1/universal/ollama/latest/actions/show-model-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/show-model-details?connectionId=$CONNECTION_ID&model=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ollama/latest/actions/show-model-details?${params}`, {
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
| `verbose` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": [
        "string"
      ],
      "details": {},
      "license": "string",
      "modelInfo": {},
      "modifiedAt": "string",
      "parameters": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | array<string> |  |
| `details` | object |  |
| `license` | string |  |
| `modelInfo` | object |  |
| `modifiedAt` | string |  |
| `parameters` | string |  |

## Native endpoint

Through the native Ollama API, this operation is `POST /api/show` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-model-details.md) for the provider-specific parameters and requirements.

