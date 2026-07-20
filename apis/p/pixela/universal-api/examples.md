# Pixela Universal API Examples

These examples use the MindCloud API key and Pixela connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Graphs

Retrieves all graph definitions in Pixela.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graphs?connectionId=$CONNECTION_ID&username=a-know" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "a-know"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graphs?${params}`, {
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
      "color": "string",
      "description": "string",
      "id": "string",
      "isSecret": true,
      "name": "Ava Chen",
      "publishOptionalData": true,
      "purgeCacheURLs": [
        "https://example.com"
      ],
      "selfSufficient": "string",
      "startOnMonday": true,
      "timezone": "string",
      "type": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Graphs action reference](actions/list-graphs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixela/latest/actions/list-graphs).

## Add To Pixel

Adds quantity to today's Pixela pixel using the graph timezone.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/add-to-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "graph_id": "string",
  "quantity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixela/latest/actions/add-to-pixel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "graph_id": "string",
    "quantity": "string"
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
      "isSuccess": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add To Pixel action reference](actions/add-to-pixel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixela/latest/actions/add-to-pixel).
