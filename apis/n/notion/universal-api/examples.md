# Notion Universal API Examples

These examples use the MindCloud API key and Notion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Bot User

Retrieves the current bot user from Notion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-bot-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-bot-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "bot": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "person": {},
      "requestId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Bot User action reference](actions/retrieve-bot-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notion/latest/actions/retrieve-bot-user).

## Append Block Children

Appends child blocks to a Notion block.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/append-block-children" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blockId": "string",
  "children": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/append-block-children', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blockId": "string",
    "children": {}
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
      "block": {},
      "hasMore": true,
      "nextCursor": "string",
      "object": "string",
      "requestId": "string",
      "results": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Append Block Children action reference](actions/append-block-children.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notion/latest/actions/append-block-children).
