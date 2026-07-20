# Pinecone: Describe Model

Retrieves details for a Pinecone model.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-model?connectionId=$CONNECTION_ID&modelName=multilingual-e5-large" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelName": "multilingual-e5-large"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-model?${params}`, {
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
| `modelName` | string | yes | The name of the model to describe. Example: `multilingual-e5-large`. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_dimension` | number |  |
| `max_batch_size` | number |  |
| `max_sequence_length` | number |  |
| `modality` | string |  |
| `model` | string |  |
| `provider_name` | string |  |
| `short_description` | string |  |
| `supported_dimensions[]` | number |  |
| `supported_metrics[]` | string |  |
| `supported_parameters[].parameter` | string |  |
| `supported_parameters[].required` | boolean |  |
| `supported_parameters[].type` | string |  |
| `supported_parameters[].value_type` | string |  |
| `type` | string |  |
| `vector_type` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /models/:model_name` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-model.md) for the provider-specific parameters and requirements.

