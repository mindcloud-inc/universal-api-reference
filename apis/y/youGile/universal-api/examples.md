# YouGile Universal API Examples

These examples use the MindCloud API key and YouGile connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List tasks

Retrieves a list of tasks from YouGile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-tasks?${params}`, {
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
      "content": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

See the full [List tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youGile/latest/actions/list-tasks).

## Create board

Creates a new board in YouGile.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youGile/latest/actions/create-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "projectId": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create board action reference](actions/create-board.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youGile/latest/actions/create-board).
