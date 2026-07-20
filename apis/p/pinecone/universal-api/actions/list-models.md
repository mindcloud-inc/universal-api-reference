# Pinecone: List Models

Retrieves available inference models from Pinecone.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-models?${params}`, {
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
| `type` | string | no | Optional model type filter: embed or rerank. Example: `embed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vectorType` | string | no | Optional embedding vector type filter: dense or sparse. Example: `dense`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "models": [
        {
          "default_dimension": 1,
          "max_batch_size": 1,
          "max_sequence_length": 1,
          "modality": "string",
          "model": "string",
          "provider_name": "Ava Chen",
          "short_description": "string",
          "supported_dimensions": [
            1
          ],
          "supported_metrics": [
            "string"
          ],
          "supported_parameters": [
            {
              "parameter": "string",
              "required": true,
              "type": "string",
              "value_type": "string"
            }
          ],
          "type": "string",
          "vector_type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `models[].default_dimension` | number |  |
| `models[].max_batch_size` | number |  |
| `models[].max_sequence_length` | number |  |
| `models[].modality` | string |  |
| `models[].model` | string |  |
| `models[].provider_name` | string |  |
| `models[].short_description` | string |  |
| `models[].supported_dimensions[]` | number |  |
| `models[].supported_metrics[]` | string |  |
| `models[].supported_parameters[].parameter` | string |  |
| `models[].supported_parameters[].required` | boolean |  |
| `models[].supported_parameters[].type` | string |  |
| `models[].supported_parameters[].value_type` | string |  |
| `models[].type` | string |  |
| `models[].vector_type` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /models` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

