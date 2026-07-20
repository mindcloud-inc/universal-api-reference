# Dubble Universal API Examples

These examples use the MindCloud API key and Dubble connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Collections

Retrieves a list of collections from Dubble.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubble/latest/actions/list-collections?${params}`, {
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

See the full [List Collections action reference](actions/list-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dubble/latest/actions/list-collections).

## Add Guide to Collection

Adds a guide to a collection in Dubble.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/add-guide-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "guideId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dubble/latest/actions/add-guide-to-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "guideId": "string"
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

See the full [Add Guide to Collection action reference](actions/add-guide-to-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dubble/latest/actions/add-guide-to-collection).
