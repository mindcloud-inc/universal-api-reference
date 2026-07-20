# Teamhood Universal API Examples

These examples use the MindCloud API key and Teamhood connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves all accessible workspaces from Teamhood.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-workspaces?${params}`, {
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
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamhood/latest/actions/list-workspaces).

## Create Item

Creates a new item in Teamhood.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/create-item', {
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
      "boardId": "string",
      "displayId": "string",
      "id": "string",
      "parentId": "string",
      "rowId": "string",
      "statusId": "string",
      "title": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Item action reference](actions/create-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamhood/latest/actions/create-item).
