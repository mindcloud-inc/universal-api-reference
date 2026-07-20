# Liveblocks Universal API Examples

These examples use the MindCloud API key and Liveblocks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Rooms

Retrieves rooms from Liveblocks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-rooms?${params}`, {
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
      "data": [
        {}
      ],
      "nextCursor": "string",
      "nextPage": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Rooms action reference](actions/get-rooms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveblocks/latest/actions/get-rooms).

## Add Comment Reaction

Creates a comment reaction in Liveblocks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/add-comment-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/add-comment-reaction', {
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
      "attachments": [
        {}
      ],
      "body": {},
      "createdAt": "string",
      "deletedAt": "string",
      "editedAt": "string",
      "id": "string",
      "metadata": {},
      "reactions": [
        {}
      ],
      "roomId": "string",
      "threadId": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment Reaction action reference](actions/add-comment-reaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveblocks/latest/actions/add-comment-reaction).
