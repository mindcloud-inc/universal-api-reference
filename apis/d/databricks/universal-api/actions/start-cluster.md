# Databricks: Start Cluster

Starts an existing cluster in the Databricks workspace.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-cluster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-cluster" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clusterId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-cluster', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clusterId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clusterId` | string | yes | The cluster to be started. |

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

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.1/clusters/start` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-cluster.md) for the provider-specific parameters and requirements.

