# Weaviate Vector Store: Get Cluster Nodes

Retrieves node status from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-cluster-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-cluster-nodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-cluster-nodes?${params}`, {
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
      "nodes": [
        {
          "batchStats": {
            "ratePerSecond": 1
          },
          "gitHash": "string",
          "name": "Ava Chen",
          "operationalMode": "string",
          "status": "string",
          "version": "string"
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
| `nodes[].batchStats.ratePerSecond` | number |  |
| `nodes[].gitHash` | string |  |
| `nodes[].name` | string |  |
| `nodes[].operationalMode` | string |  |
| `nodes[].status` | string |  |
| `nodes[].version` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /v1/nodes` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cluster-nodes.md) for the provider-specific parameters and requirements.

