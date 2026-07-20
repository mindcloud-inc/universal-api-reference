# Pinecone: Create Index With Integrated Embedding

Creates an index with integrated embedding in Pinecone.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index-with-integrated-embedding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index-with-integrated-embedding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "cloud": "aws",
  "region": "us-east-1",
  "embed": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index-with-integrated-embedding', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "cloud": "aws",
    "region": "us-east-1",
    "embed": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the index to create. |
| `cloud` | string | yes | The cloud provider where the index is hosted. Example: `aws`. |
| `region` | string | yes | The region where the index is created. Example: `us-east-1`. |
| `embed` | object | yes | The integrated embedding configuration object, including model, field map, and read/write parameters. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deletionProtection` | string | no | Whether deletion protection is enabled for the index. Default: `disabled`. Example: `disabled`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletion_protection": "string",
      "dimension": 1,
      "embed": {
        "dimension": 1,
        "field_map": {
          "text": "string"
        },
        "metric": "string",
        "model": "string",
        "read_parameters": {
          "dimension": 1,
          "input_type": "string",
          "truncate": "string"
        },
        "vector_type": "string",
        "write_parameters": {
          "dimension": 1,
          "input_type": "string",
          "truncate": "string"
        }
      },
      "host": "string",
      "metric": "string",
      "name": "Ava Chen",
      "spec": {
        "serverless": {
          "cloud": "string",
          "read_capacity": {
            "mode": "string",
            "status": {
              "state": "string"
            }
          },
          "region": "string"
        }
      },
      "status": {
        "ready": true,
        "state": "string"
      },
      "vector_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletion_protection` | string |  |
| `dimension` | number |  |
| `embed.dimension` | number |  |
| `embed.field_map.text` | string |  |
| `embed.metric` | string |  |
| `embed.model` | string |  |
| `embed.read_parameters.dimension` | number |  |
| `embed.read_parameters.input_type` | string |  |
| `embed.read_parameters.truncate` | string |  |
| `embed.vector_type` | string |  |
| `embed.write_parameters.dimension` | number |  |
| `embed.write_parameters.input_type` | string |  |
| `embed.write_parameters.truncate` | string |  |
| `host` | string |  |
| `metric` | string |  |
| `name` | string |  |
| `spec.serverless.cloud` | string |  |
| `spec.serverless.read_capacity.mode` | string |  |
| `spec.serverless.read_capacity.status.state` | string |  |
| `spec.serverless.region` | string |  |
| `status.ready` | boolean |  |
| `status.state` | string |  |
| `vector_type` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `POST /indexes/create-for-model` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-index-with-integrated-embedding.md) for the provider-specific parameters and requirements.

