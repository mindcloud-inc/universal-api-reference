# Databricks: Get SQL Warehouse

Retrieves a SQL warehouse from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-sql-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-sql-warehouse?connectionId=$CONNECTION_ID&warehouseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "warehouseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-sql-warehouse?${params}`, {
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
| `warehouseId` | string | yes | Required. Id of the SQL warehouse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_stop_mins": 1,
      "channel": {
        "dbsql_version": "string",
        "name": "Ava Chen"
      },
      "cluster_size": "string",
      "creator_name": "Ava Chen",
      "enable_photon": true,
      "enable_serverless_compute": true,
      "health": {
        "details": "string",
        "failure_reason": {
          "code": "string",
          "parameters": {},
          "type": "string"
        },
        "message": "string",
        "status": "string",
        "summary": "string"
      },
      "id": "string",
      "instance_profile_arn": "string",
      "jdbc_url": "https://example.com",
      "max_num_clusters": 1,
      "min_num_clusters": 1,
      "name": "Ava Chen",
      "num_active_sessions": 1,
      "num_clusters": 1,
      "odbc_params": {
        "hostname": "Ava Chen",
        "path": "string",
        "port": 1,
        "protocol": "string"
      },
      "spot_instance_policy": "string",
      "state": "string",
      "tags": {
        "custom_tags": [
          {
            "key": "string",
            "value": "string"
          }
        ]
      },
      "warehouse_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_stop_mins` | number | The amount of time in minutes that a SQL warehouse must be idle (i.e., no RUNNING queries) before it is automatically stopped.  Supported values: - Must be == 0 or >= 10 mins - 0 indicates no autostop.  Defaults to 120 mins |
| `channel` | object | Configures the channel name and DBSQL version of the warehouse. CHANNEL_NAME_CUSTOM should be chosen only when `dbsql_version` is specified. |
| `channel.dbsql_version` | string |  |
| `channel.name` | string |  |
| `cluster_size` | string | Size of the clusters allocated for this warehouse. Increasing the size of a spark cluster allows you to run larger queries on it. If you want to increase the number of concurrent queries, please tune max_num_clusters.  Supported values: - 2X-Small - X-Small - Small - Medium - Large - X-Large - 2X-Large - 3X-Large - 4X-Large - 5X-Large |
| `creator_name` | string | warehouse creator name |
| `enable_photon` | boolean | Configures whether the warehouse should use Photon optimized clusters.  Defaults to true. |
| `enable_serverless_compute` | boolean | Configures whether the warehouse should use serverless compute |
| `health` | object |  |
| `health.details` | string | Details about errors that are causing current degraded/failed status. |
| `health.failure_reason` | object |  |
| `health.failure_reason.code` | string | The status code indicating why the cluster was terminated |
| `health.failure_reason.parameters` | object | list of parameters that provide additional information about why the cluster was terminated |
| `health.failure_reason.type` | string | type of the termination |
| `health.message` | string | Deprecated. split into summary and details for security |
| `health.status` | string |  |
| `health.summary` | string | A short summary of the health status in case of degraded/failed warehouses. |
| `id` | string | unique identifier for warehouse |
| `instance_profile_arn` | string | Deprecated. Instance profile used to pass IAM role to the cluster |
| `jdbc_url` | string | the jdbc connection string for this warehouse |
| `max_num_clusters` | number | Maximum number of clusters that the autoscaler will create to handle concurrent queries.  Supported values: - Must be >= min_num_clusters - Must be <= 40.  Defaults to min_clusters if unset. |
| `min_num_clusters` | number | Minimum number of available clusters that will be maintained for this SQL warehouse. Increasing this will ensure that a larger number of clusters are always running and therefore may reduce the cold start time for new queries. This is similar to reserved vs. revocable cores in a resource manager.  Supported values: - Must be > 0 - Must be <= min(max_num_clusters, 30)  Defaults to 1 |
| `name` | string | Logical name for the cluster.  Supported values: - Must be unique within an org. - Must be less than 100 characters. |
| `num_active_sessions` | number | Deprecated. current number of active sessions for the warehouse |
| `num_clusters` | number | current number of clusters running for the service |
| `odbc_params` | object |  |
| `odbc_params.hostname` | string |  |
| `odbc_params.path` | string |  |
| `odbc_params.port` | number |  |
| `odbc_params.protocol` | string |  |
| `spot_instance_policy` | string | EndpointSpotInstancePolicy configures whether the endpoint should use spot instances.  The breakdown of how the EndpointSpotInstancePolicy converts to per cloud configurations is:  +-------+--------------------------------------+--------------------------------+ \| Cloud \|            COST_OPTIMIZED            \|     RELIABILITY_OPTIMIZED \| +-------+--------------------------------------+--------------------------------+ \| AWS   \| On Demand Driver with Spot Executors \| On Demand Driver and Executors \| \| AZURE \| On Demand Driver and Executors       \| On Demand Driver and Executors \| +-------+--------------------------------------+--------------------------------+  While including "spot" in the enum name may limit the the future extensibility of this field because it limits this enum to denoting "spot or not", this is the field that PM recommends after discussion with customers per SC-48783. |
| `state` | string | * State of a warehouse. |
| `tags` | object |  |
| `tags.custom_tags` | array<string> |  |
| `tags.custom_tags[].key` | string |  |
| `tags.custom_tags[].value` | string |  |
| `warehouse_type` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.0/sql/warehouses/:warehouseId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sql-warehouse.md) for the provider-specific parameters and requirements.

