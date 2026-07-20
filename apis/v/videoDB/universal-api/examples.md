# VideoDB Universal API Examples

These examples use the MindCloud API key and VideoDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Videos

Retrieves videos from VideoDB.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-videos?${params}`, {
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
      "collection_id": "string",
      "id": "string",
      "length": "string",
      "name": "Ava Chen",
      "player_link": "https://example.com",
      "player_url": "https://example.com",
      "size": "string",
      "stream_link": "https://example.com",
      "stream_url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Videos action reference](actions/list-videos.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/videoDB/latest/actions/list-videos).

## Create Collection

Creates a new collection in VideoDB.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "description": "string",
      "id": "string",
      "is_public": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/videoDB/latest/actions/create-collection).
