# Qdrant Universal API Examples

These examples use the MindCloud API key and Qdrant connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Collections

Retrieves all existing collections from Qdrant.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qdrant/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qdrant/latest/actions/list-collections?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Collections action reference](actions/list-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qdrant/latest/actions/list-collections).
