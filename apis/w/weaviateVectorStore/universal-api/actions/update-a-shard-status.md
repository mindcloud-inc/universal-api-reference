# Weaviate Vector Store: Update a shard status

Updates a shard status in Weaviate.

```
PUT https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/update-a-shard-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/update-a-shard-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classname": "Ava Chen",
  "shardname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/update-a-shard-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classname": "Ava Chen",
    "shardname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classname` | string | yes | The name of the collection (class) containing the shard. |
| `shardname` | string | yes | The name of the shard to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `PUT /schema/:className/shards/:shardName` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-shard-status.md) for the provider-specific parameters and requirements.

