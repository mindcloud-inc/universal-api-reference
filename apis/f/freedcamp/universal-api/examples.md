# Freedcamp Universal API Examples

These examples use the MindCloud API key and Freedcamp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves a list of projects from Freedcamp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/list-projects?${params}`, {
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

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freedcamp/latest/actions/list-projects).

## Create Comment

Creates a new task comment in Freedcamp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task_id": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task_id": "string",
    "description": "string"
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
      "itemId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freedcamp/latest/actions/create-comment).
