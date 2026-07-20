# Pinterest Universal API Examples

These examples use the MindCloud API key and Pinterest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Boards

Retrieves the current user's boards from Pinterest.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-boards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-boards?${params}`, {
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
      "boardPinsModifiedAt": "2026-05-07T12:00:00.000Z",
      "collaboratorCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "followerCount": 1,
      "id": "string",
      "media": {
        "imageCoverUrl": "https://example.com",
        "pinThumbnailUrls": [
          "https://example.com"
        ]
      },
      "name": "Ava Chen",
      "owner": {
        "username": "Ava Chen"
      },
      "pinCount": 1,
      "privacy": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Boards action reference](actions/list-boards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinterest/latest/actions/list-boards).

## Create Board

Creates a new board in Pinterest.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/create-board', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Board action reference](actions/create-board.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinterest/latest/actions/create-board).
