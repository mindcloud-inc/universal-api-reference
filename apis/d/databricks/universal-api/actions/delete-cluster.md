# Databricks: Delete Cluster

Deletes an existing cluster from the Databricks workspace.

```
DELETE https://connect.mindcloud.co/v1/universal/databricks/latest/actions/delete-cluster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/delete-cluster?connectionId=$CONNECTION_ID&clusterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clusterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/delete-cluster?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clusterId` | string | yes | The cluster to be terminated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_id": "string",
      "cluster_name": "Ava Chen",
      "state": "string",
      "state_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_id` | string | Canonical identifier for the cluster. |
| `cluster_name` | string | Cluster name. |
| `state` | string | Current cluster state. |
| `state_message` | string | State transition message. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.1/clusters/delete` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-cluster.md) for the provider-specific parameters and requirements.

