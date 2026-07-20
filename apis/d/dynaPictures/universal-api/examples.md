# DynaPictures Universal API Examples

These examples use the MindCloud API key and DynaPictures connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from DynaPictures.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/list-workspaces?${params}`, {
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

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynaPictures/latest/actions/list-workspaces).

## Create Workspace

Creates a workspace in DynaPictures.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/create-workspace', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Workspace action reference](actions/create-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynaPictures/latest/actions/create-workspace).
