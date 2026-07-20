# Pinecone: Create Index

Creates a new index in Pinecone.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "vectorType": "dense",
  "dimension": "8",
  "metric": "cosine",
  "spec": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "vectorType": "dense",
    "dimension": "8",
    "metric": "cosine",
    "spec": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the index to create. |
| `vectorType` | string | yes | The vector type for the index. Example: `dense`. |
| `dimension` | number | yes | The dimension for dense vectors in the index. Example: `8`. |
| `metric` | string | yes | The similarity metric for the index. Example: `cosine`. |
| `spec` | object | yes | The index specification object, such as a serverless or BYOC deployment spec. |

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

Through the native Pinecone API, this operation is `POST /indexes` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-index.md) for the provider-specific parameters and requirements.

