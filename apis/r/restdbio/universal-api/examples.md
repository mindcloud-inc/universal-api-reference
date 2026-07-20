# Restdb.io Universal API Examples

These examples use the MindCloud API key and Restdb.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Database Metadata

Retrieves database metadata from Restdb.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-database-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-database-metadata?${params}`, {
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
      "collections": [
        "string"
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Database Metadata action reference](actions/get-database-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/restdbio/latest/actions/get-database-metadata).

## Bulk Create Documents

Creates multiple documents in Restdb.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/bulk-create-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collection": "string",
  "documents": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/bulk-create-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collection": "string",
    "documents": "string"
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

See the full [Bulk Create Documents action reference](actions/bulk-create-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/restdbio/latest/actions/bulk-create-documents).
