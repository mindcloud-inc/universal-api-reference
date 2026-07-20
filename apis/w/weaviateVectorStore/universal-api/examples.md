# Weaviate Vector Store Universal API Examples

These examples use the MindCloud API key and Weaviate Vector Store connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Cluster Meta

Retrieves instance metadata from Weaviate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-cluster-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-cluster-meta?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "grpcMaxMessageSize": 1,
      "hostname": "Ava Chen",
      "modules": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Cluster Meta action reference](actions/get-cluster-meta.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weaviateVectorStore/latest/actions/get-cluster-meta).

## Activate a user

Activates a user in Weaviate.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/activateuser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/activateuser', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Activate a user action reference](actions/activateuser.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weaviateVectorStore/latest/actions/activateuser).
