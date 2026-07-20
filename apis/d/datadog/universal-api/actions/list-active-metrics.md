# Datadog: List Active Metrics

Retrieves active metrics from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-active-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-active-metrics?connectionId=$CONNECTION_ID&from=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-active-metrics?${params}`, {
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
| `from` | number | yes | Seconds since the Unix epoch. |
| `host` | string | no | Hostname for filtering the metrics returned. |
| `tagFilter` | string | no | Filter metrics using tag expressions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from": "string",
      "metrics": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | string | Unix epoch lower bound used for the metric search. |
| `metrics` | array<string> | Metric names active in the time window. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/metrics` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-metrics.md) for the provider-specific parameters and requirements.

