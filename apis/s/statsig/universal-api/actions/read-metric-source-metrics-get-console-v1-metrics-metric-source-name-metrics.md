# Statsig: Read Metric Source Metrics

Retrieves metric source metrics from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics?connectionId=$CONNECTION_ID&limit=25&offset=0&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics?${params}`, {
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
| `name` | string | yes | name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Results per page |
| `page` | number | no | Page number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/metrics/metric_source/{name}/metrics` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics.md) for the provider-specific parameters and requirements.

