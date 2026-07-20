# Taskade Universal API Examples

These examples use the MindCloud API key and Taskade connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from your Taskade account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-workspaces?${params}`, {
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

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taskade/latest/actions/list-workspaces).

## Add Project To Agent Knowledge

Adds a project to a Taskade agent knowledge base.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/add-project-to-agent-knowledge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskade/latest/actions/add-project-to-agent-knowledge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
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
      "data": {},
      "id": "string",
      "name": "Ava Chen",
      "spaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Project To Agent Knowledge action reference](actions/add-project-to-agent-knowledge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taskade/latest/actions/add-project-to-agent-knowledge).
