# Recombee Universal API Examples

These examples use the MindCloud API key and Recombee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Items

Retrieves items from your Recombee catalog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recombee/latest/actions/list-items?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Items action reference](actions/list-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recombee/latest/actions/list-items).

## Add Bookmark

Creates a bookmark event in Recombee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/add-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "item-123",
  "userId": "user-123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recombee/latest/actions/add-bookmark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "item-123",
    "userId": "user-123"
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

See the full [Add Bookmark action reference](actions/add-bookmark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recombee/latest/actions/add-bookmark).
