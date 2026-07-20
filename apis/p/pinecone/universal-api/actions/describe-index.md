# Pinecone: Describe Index

Retrieves details for an index from Pinecone.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-index?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-index?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deletionProtection": "string",
      "dimension": 1,
      "embed": {
        "dimension": 1,
        "fieldMap": {
          "text": "string"
        },
        "metric": "string",
        "model": "string",
        "readParameters": {
          "dimension": 1,
          "inputType": "string",
          "truncate": "string"
        },
        "vectorType": "string",
        "writeParameters": {
          "dimension": 1,
          "inputType": "string",
          "truncate": "string"
        }
      },
      "host": "string",
      "metric": "string",
      "name": "Ava Chen",
      "spec": {
        "serverless": {
          "cloud": "string",
          "readCapacity": {
            "mode": "string",
            "status": {
              "currentReplicas": {},
              "currentShards": {},
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
      "tags": {},
      "vectorType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletionProtection` | string |  |
| `dimension` | number |  |
| `embed.dimension` | number |  |
| `embed.fieldMap.text` | string |  |
| `embed.metric` | string |  |
| `embed.model` | string |  |
| `embed.readParameters.dimension` | number |  |
| `embed.readParameters.inputType` | string |  |
| `embed.readParameters.truncate` | string |  |
| `embed.vectorType` | string |  |
| `embed.writeParameters.dimension` | number |  |
| `embed.writeParameters.inputType` | string |  |
| `embed.writeParameters.truncate` | string |  |
| `host` | string |  |
| `metric` | string |  |
| `name` | string |  |
| `spec.serverless.cloud` | string |  |
| `spec.serverless.readCapacity.mode` | string |  |
| `spec.serverless.readCapacity.status.currentReplicas` | object |  |
| `spec.serverless.readCapacity.status.currentShards` | object |  |
| `spec.serverless.readCapacity.status.state` | string |  |
| `spec.serverless.region` | string |  |
| `status.ready` | boolean |  |
| `status.state` | string |  |
| `tags` | object |  |
| `vectorType` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /indexes/:index_name` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-index.md) for the provider-specific parameters and requirements.

