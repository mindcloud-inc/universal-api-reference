# DeployHQ Universal API Examples

These examples use the MindCloud API key and DeployHQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves all projects from DeployHQ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-projects?${params}`, {
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
      "app_url": "https://example.com",
      "auto_deploy_url": "https://example.com",
      "build_commands_url": "https://example.com",
      "config_files_url": "https://example.com",
      "deployments_url": "https://example.com",
      "environment_variables_url": "https://example.com",
      "identifier": "string",
      "last_deployed_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "public_key": "string",
      "repository": "string",
      "repository_url": "https://example.com",
      "servers_url": "https://example.com",
      "starred": true,
      "url": "https://example.com",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deployHQ/latest/actions/list-projects).

## Abort Deployment

Aborts a running deployment in DeployHQ.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/abort-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/abort-deployment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "id": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Abort Deployment action reference](actions/abort-deployment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deployHQ/latest/actions/abort-deployment).
