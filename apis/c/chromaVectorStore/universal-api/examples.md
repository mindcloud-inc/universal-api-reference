# Chroma Vector Store Universal API Examples

These examples use the MindCloud API key and Chroma Vector Store connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Identity

Retrieves user identity details from Chroma.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/get-user-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/get-user-identity?${params}`, {
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
      "databases": [
        "string"
      ],
      "tenant": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Identity action reference](actions/get-user-identity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chromaVectorStore/latest/actions/get-user-identity).

## Create Collection

Creates a new collection in Chroma.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "database": "string",
  "name": "Ava Chen",
  "tenant": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "database": "string",
    "name": "Ava Chen",
    "tenant": "string"
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
      "configuration_json": {},
      "database": "string",
      "dimension": 1,
      "id": "string",
      "log_position": 1,
      "metadata": {},
      "name": "Ava Chen",
      "schema": {},
      "tenant": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chromaVectorStore/latest/actions/create-collection).
