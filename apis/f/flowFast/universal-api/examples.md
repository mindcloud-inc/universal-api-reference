# FlowFast Universal API Examples

These examples use the MindCloud API key and FlowFast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Spaces

Retrieves spaces from FlowFast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/list-spaces?${params}`, {
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
      "archived": true,
      "id": 1,
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Spaces action reference](actions/list-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowFast/latest/actions/list-spaces).

## Create Board

Creates a new board in FlowFast.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/create-board', {
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
      "defaultCardTypeId": 1,
      "id": 1,
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Board action reference](actions/create-board.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowFast/latest/actions/create-board).
