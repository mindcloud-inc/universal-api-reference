# Cerebras AI: Retrieve Public Model

Retrieves a public model from Cerebras AI.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model?${params}`, {
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
      "architecture": {},
      "capabilities": {},
      "created": 1,
      "datacenterLocations": [
        {}
      ],
      "deprecated": true,
      "description": "string",
      "huggingFaceId": "string",
      "id": "string",
      "limits": {},
      "name": "Ava Chen",
      "object": "string",
      "ownedBy": "string",
      "preview": true,
      "pricing": {},
      "quantization": "string",
      "supportedParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `architecture` | object |  |
| `capabilities` | object |  |
| `created` | number |  |
| `datacenterLocations` | array<object> |  |
| `deprecated` | boolean |  |
| `description` | string |  |
| `huggingFaceId` | string |  |
| `id` | string |  |
| `limits` | object |  |
| `name` | string |  |
| `object` | string |  |
| `ownedBy` | string |  |
| `preview` | boolean |  |
| `pricing` | object |  |
| `quantization` | string |  |
| `supportedParameters` | object |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET /public/v1/models/:modelId` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-public-model.md) for the provider-specific parameters and requirements.

