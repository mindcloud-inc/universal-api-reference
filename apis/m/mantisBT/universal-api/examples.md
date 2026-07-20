# MantisBT Universal API Examples

These examples use the MindCloud API key and MantisBT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My User Info

Retrieves the current user from MantisBT.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-my-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-my-user-info?${params}`, {
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

See the full [Get My User Info action reference](actions/get-my-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mantisBT/latest/actions/get-my-user-info).

## Create Issue

Creates a new issue in MantisBT.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category.name": "Ava Chen",
  "description": "string",
  "project.id": 1,
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category.name": "Ava Chen",
    "description": "string",
    "project.id": 1,
    "summary": "string"
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

See the full [Create Issue action reference](actions/create-issue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mantisBT/latest/actions/create-issue).
