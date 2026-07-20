# Asana Universal API Examples

These examples use the MindCloud API key and Asana connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get multiple workspaces

Retrieves workspaces from Asana.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-multiple-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-multiple-workspaces?${params}`, {
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
      "gid": "string",
      "name": "Ava Chen",
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get multiple workspaces action reference](actions/get-multiple-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/asanaNew/latest/actions/get-multiple-workspaces).

## Add a collaborator to a goal

Adds a collaborator to a goal in Asana.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-collaborator-to-a-goal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataFollowers": "string",
  "goalGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-collaborator-to-a-goal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataFollowers": "string",
    "goalGid": "string"
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

See the full [Add a collaborator to a goal action reference](actions/add-a-collaborator-to-a-goal.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/asanaNew/latest/actions/add-a-collaborator-to-a-goal).
