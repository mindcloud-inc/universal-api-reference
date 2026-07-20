# Inistate Universal API Examples

These examples use the MindCloud API key and Inistate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspace

Retrieves a workspace from Inistate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-workspace?${params}`, {
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

See the full [Get Workspace action reference](actions/get-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inistate/latest/actions/get-workspace).

## Create Stage0 Entry

Creates a new Stage0 entry in Inistate.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/create-stage0-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inistate/latest/actions/create-stage0-entry', {
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
      "activityId": "string",
      "collection": "string",
      "entryId": 1,
      "result": {},
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Stage0 Entry action reference](actions/create-stage0-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inistate/latest/actions/create-stage0-entry).
