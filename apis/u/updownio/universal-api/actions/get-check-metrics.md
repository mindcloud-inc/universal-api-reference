# updown.io: Get Check Metrics

Retrieves detailed check metrics from updown.io.

```
GET https://connect.mindcloud.co/v1/universal/updownio/latest/actions/get-check-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/get-check-metrics?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/get-check-metrics?${params}`, {
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
| `from` | date | no | Start time for the metrics window. |
| `group` | list | no | Group data by time or host. One of: `host`, `time`. |
| `to` | date | no | End time for the metrics window. |
| `token` | string | yes | The check unique token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apdex": 1,
      "requests": {},
      "timings": {},
      "uptime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apdex` | number | APDEX score over the metrics window. |
| `requests` | object | Request volume and latency-bucket metrics. |
| `timings` | object | Timing breakdown metrics. |
| `uptime` | number | Uptime percentage over the metrics window. |

## Native endpoint

Through the native updown.io API, this operation is `GET /checks/:token/metrics` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-check-metrics.md) for the provider-specific parameters and requirements.

