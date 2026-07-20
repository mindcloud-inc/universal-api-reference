# Milvus Vector Store Universal API Examples

These examples use the MindCloud API key and Milvus Vector Store connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Databases

Retrieves databases from Milvus Vector Store.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/list-databases?${params}`, {
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
      "code": 1,
      "data": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Databases action reference](actions/list-databases.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/milvusVectorStore/latest/actions/list-databases).

## Alter Alias

Updates an alias in Milvus Vector Store.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/alter-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/alter-alias', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Alter Alias action reference](actions/alter-alias.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/milvusVectorStore/latest/actions/alter-alias).
