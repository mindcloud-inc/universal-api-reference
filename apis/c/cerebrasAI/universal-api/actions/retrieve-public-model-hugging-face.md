# Cerebras AI: Retrieve Public Model (HuggingFace)

Retrieves a HuggingFace-formatted public model from Cerebras AI.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model-hugging-face
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model-hugging-face?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model-hugging-face?${params}`, {
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
| `modelId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contextLength": 1,
      "created": 1,
      "datacenters": [
        {}
      ],
      "description": "string",
      "huggingFaceId": "string",
      "id": "string",
      "inputModalities": [
        "string"
      ],
      "maxOutputLength": 1,
      "name": "Ava Chen",
      "outputModalities": [
        "string"
      ],
      "pricing": {},
      "quantization": "string",
      "supportedFeatures": [
        "string"
      ],
      "supportedSamplingParameters": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextLength` | number |  |
| `created` | number |  |
| `datacenters` | array<object> |  |
| `description` | string |  |
| `huggingFaceId` | string |  |
| `id` | string |  |
| `inputModalities` | array<string> |  |
| `maxOutputLength` | number |  |
| `name` | string |  |
| `outputModalities` | array<string> |  |
| `pricing` | object |  |
| `quantization` | string |  |
| `supportedFeatures` | array<string> |  |
| `supportedSamplingParameters` | array<string> |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET /public/v1/models/:modelId` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-public-model-hugging-face.md) for the provider-specific parameters and requirements.

