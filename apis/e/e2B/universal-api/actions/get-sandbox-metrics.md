# E2B: Get Sandbox Metrics

Retrieves metrics for a sandbox from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-sandbox-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-sandbox-metrics?connectionId=$CONNECTION_ID&sandboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-sandbox-metrics?${params}`, {
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
| `sandboxId` | string | yes | Identifier of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cpuCount": 1,
      "cpuUsedPct": 1,
      "diskTotal": 1,
      "diskUsed": 1,
      "memCache": 1,
      "memTotal": 1,
      "memUsed": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "timestampUnix": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cpuCount` | number | Number of CPU cores. |
| `cpuUsedPct` | number | CPU usage percentage. |
| `diskTotal` | number | Total disk space in bytes. |
| `diskUsed` | number | Disk used in bytes. |
| `memCache` | number | Cached memory in bytes. |
| `memTotal` | number | Total memory in bytes. |
| `memUsed` | number | Memory used in bytes. |
| `timestamp` | date | Deprecated timestamp of the metric entry. |
| `timestampUnix` | number | Metric timestamp as Unix seconds. |

## Native endpoint

Through the native E2B API, this operation is `GET /sandboxes/{sandboxID}/metrics` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sandbox-metrics.md) for the provider-specific parameters and requirements.

