# ClickHouse: Get ClickPipe Settings



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-click-pipe-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-click-pipe-settings?connectionId=$CONNECTION_ID&organizationId=string&serviceId=string&clickPipeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "serviceId": "string",
  "clickPipeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-click-pipe-settings?${params}`, {
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
| `organizationId` | string | yes | ID of the organization that owns the service. |
| `serviceId` | string | yes | ID of the requested service. |
| `clickPipeId` | string | yes | ID of the requested ClickPipe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickhouse_max_download_threads": 1,
      "clickhouse_max_insert_threads": 1,
      "clickhouse_max_threads": 1,
      "clickhouse_min_insert_block_size_bytes": 1,
      "clickhouse_parallel_distributed_insert_select": 1,
      "clickhouse_parallel_view_processing": true,
      "object_storage_concurrency": 1,
      "object_storage_max_file_count": 1,
      "object_storage_max_insert_bytes": 1,
      "object_storage_polling_interval_ms": 1,
      "object_storage_use_cluster_function": true,
      "streaming_max_insert_wait_ms": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickhouse_max_download_threads` | number | Maximum concurrent download threads. |
| `clickhouse_max_insert_threads` | number | Maximum concurrent ClickHouse insert threads. |
| `clickhouse_max_threads` | number | Maximum concurrent ClickHouse file-processing threads. |
| `clickhouse_min_insert_block_size_bytes` | number | Minimum insert block size in bytes. |
| `clickhouse_parallel_distributed_insert_select` | number | Parallel distributed insert-select setting. |
| `clickhouse_parallel_view_processing` | boolean | Whether attached views are processed concurrently. |
| `object_storage_concurrency` | number | Number of concurrent object-storage file processing threads. |
| `object_storage_max_file_count` | number | Maximum files processed in a single object-storage insert batch. |
| `object_storage_max_insert_bytes` | number | Maximum bytes processed in a single object-storage insert batch. |
| `object_storage_polling_interval_ms` | number | Object-storage polling interval in milliseconds. |
| `object_storage_use_cluster_function` | boolean | Whether to use the ClickHouse cluster function for distributed processing. |
| `streaming_max_insert_wait_ms` | number | Streaming max insert wait time in milliseconds. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/services/[:serviceId]/clickpipes/[:clickPipeId]/settings` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-click-pipe-settings.md) for the provider-specific parameters and requirements.

