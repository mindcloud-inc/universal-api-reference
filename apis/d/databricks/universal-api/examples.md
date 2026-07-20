# Databricks Universal API Examples

These examples use the MindCloud API key and Databricks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from the Databricks account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspaces?${params}`, {
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
      "account_id": "string",
      "aws_region": "string",
      "compute_mode": "string",
      "creation_time": 1,
      "deployment_name": "Ava Chen",
      "identity_federation_info": {},
      "is_no_public_ip_enabled": true,
      "pricing_tier": "string",
      "workspace_fqdn": "string",
      "workspace_id": 1,
      "workspace_info": {},
      "workspace_name": "Ava Chen",
      "workspace_status": "string",
      "workspace_status_message": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/databricks/latest/actions/list-workspaces).

## Create Cluster

Creates a new cluster in the Databricks workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-cluster" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloneFrom.sourceClusterId": "string",
  "initScripts": "string",
  "sparkVersion": "string",
  "sshPublicKeys": "string",
  "workloadType.clients": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-cluster', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloneFrom.sourceClusterId": "string",
    "initScripts": "string",
    "sparkVersion": "string",
    "sshPublicKeys": "string",
    "workloadType.clients": {}
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
      "cluster_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Cluster action reference](actions/create-cluster.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/databricks/latest/actions/create-cluster).
