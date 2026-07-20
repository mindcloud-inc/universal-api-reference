# Statsig: Read Single Metric Value

Retrieves a single metric value from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-single-metric-value-get-console-v1-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-single-metric-value-get-console-v1-metrics?connectionId=$CONNECTION_ID&id=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-single-metric-value-get-console-v1-metrics?${params}`, {
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
| `id` | string | yes | The unique identifier of the metric with format <metric_id>::<type> |
| `date` | string | yes | Expected valid date in the form of YYYY-MM-DD |

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

Through the native Statsig API, this operation is `GET /console/v1/metrics` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-single-metric-value-get-console-v1-metrics.md) for the provider-specific parameters and requirements.

