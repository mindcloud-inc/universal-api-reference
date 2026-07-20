# Pinecone: List Indexes

Retrieves indexes for a Pinecone project.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-indexes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-indexes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-indexes?${params}`, {
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
      "indexes": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `indexes[].deletionProtection` | string |  |
| `indexes[].dimension` | number |  |
| `indexes[].embed.dimension` | number |  |
| `indexes[].embed.fieldMap.text` | string |  |
| `indexes[].embed.metric` | string |  |
| `indexes[].embed.model` | string |  |
| `indexes[].embed.readParameters.dimension` | number |  |
| `indexes[].embed.readParameters.inputType` | string |  |
| `indexes[].embed.readParameters.truncate` | string |  |
| `indexes[].embed.vectorType` | string |  |
| `indexes[].embed.writeParameters.dimension` | number |  |
| `indexes[].embed.writeParameters.inputType` | string |  |
| `indexes[].embed.writeParameters.truncate` | string |  |
| `indexes[].host` | string |  |
| `indexes[].metric` | string |  |
| `indexes[].name` | string |  |
| `indexes[].spec.serverless.cloud` | string |  |
| `indexes[].spec.serverless.readCapacity.mode` | string |  |
| `indexes[].spec.serverless.readCapacity.status.currentReplicas` | object |  |
| `indexes[].spec.serverless.readCapacity.status.currentShards` | object |  |
| `indexes[].spec.serverless.readCapacity.status.state` | string |  |
| `indexes[].spec.serverless.region` | string |  |
| `indexes[].status.ready` | boolean |  |
| `indexes[].status.state` | string |  |
| `indexes[].tags` | object |  |
| `indexes[].vectorType` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /indexes` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-indexes.md) for the provider-specific parameters and requirements.

