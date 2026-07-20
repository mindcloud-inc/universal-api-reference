# Mem0 Universal API Examples

These examples use the MindCloud API key and Mem0 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Mem0.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-organizations?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mem0/latest/actions/list-organizations).

## Add Memories



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/add-memories" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mem0/latest/actions/add-memories', {
  method: 'POST',
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
      "data": {},
      "event": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Memories action reference](actions/add-memories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mem0/latest/actions/add-memories).
