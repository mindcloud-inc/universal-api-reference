# OpnForm Universal API Examples

These examples use the MindCloud API key and OpnForm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Lists all workspaces in the OpnForm account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/list-workspaces?${params}`, {
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
      "icon": "string",
      "id": 1,
      "name": "Ava Chen",
      "pivot": {},
      "settings": [
        {}
      ],
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/opnForm/latest/actions/list-workspaces).

## Add Workspace User

Adds a user to an OpnForm workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/add-workspace-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "email": "ava@example.com",
  "role": "user"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/add-workspace-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "email": "ava@example.com",
    "role": "user"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Workspace User action reference](actions/add-workspace-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/opnForm/latest/actions/add-workspace-user).
