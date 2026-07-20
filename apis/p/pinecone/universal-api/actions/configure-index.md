# Pinecone: Configure Index

Updates an existing index in Pinecone.

```
PUT https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/configure-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/configure-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/configure-index', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | The name of the index to configure. |
| `tags` | object | no | Custom tags to add or update on the index. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deletionProtection` | string | no | Whether deletion protection is enabled or disabled for the index. Example: `enabled`. |
| `spec` | object | no | The scaling or deployment specification updates for the index. |
| `embed` | object | no | The integrated embedding configuration updates for the index. |

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
      "tags": {
        "kind": "string",
        "stage": "string"
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
| `tags.kind` | string |  |
| `tags.stage` | string |  |
| `vector_type` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `PATCH /indexes/:index_name` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-index.md) for the provider-specific parameters and requirements.

