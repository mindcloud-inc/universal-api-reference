# Daytona: Get Sandbox Metrics

Retrieves sandbox metrics from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-metrics?connectionId=$CONNECTION_ID&sandboxId=string&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxId": "string",
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-metrics?${params}`, {
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
| `sandboxId` | string | yes | ID of the sandbox. |
| `from` | date | yes | Start of time range (ISO 8601). |
| `to` | date | yes | End of time range (ISO 8601). |
| `metricNames[]` | array<string> | no | Filter by metric names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "series": [
        {
          "dataPoints": [
            {
              "timestamp": "2026-05-07T12:00:00.000Z",
              "value": 1
            }
          ],
          "metricName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `series` | array<object> | List of metric series. |
| `series[].dataPoints` | array<object> | Data points for this metric. |
| `series[].dataPoints[].timestamp` | date | Timestamp of the data point. |
| `series[].dataPoints[].value` | number | Value at this timestamp. |
| `series[].metricName` | string | Name of the metric. |

## Native endpoint

Through the native Daytona API, this operation is `GET /sandbox/[:sandboxId]/telemetry/metrics` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sandbox-metrics.md) for the provider-specific parameters and requirements.

