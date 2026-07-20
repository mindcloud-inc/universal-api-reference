# New Relic: Get Application Metric Timeslice Data

Retrieves application metric timeslice data from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-application-metric-timeslice-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-application-metric-timeslice-data?connectionId=$CONNECTION_ID&appId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-application-metric-timeslice-data?${params}`, {
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
| `appId` | number | yes | New Relic application ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metric_data": {
        "from": "2026-05-07T12:00:00.000Z",
        "metrics_found": "string",
        "metrics_not_found": "string",
        "metrics": [
          {
            "name": "Ava Chen",
            "timeslices": [
              {
                "from": "2026-05-07T12:00:00.000Z",
                "to": "2026-05-07T12:00:00.000Z"
              }
            ]
          }
        ],
        "to": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metric_data.from` | date |  |
| `metric_data.metrics_found` | string |  |
| `metric_data.metrics_not_found` | string |  |
| `metric_data.metrics[].name` | string |  |
| `metric_data.metrics[].timeslices[].from` | date |  |
| `metric_data.metrics[].timeslices[].to` | date |  |
| `metric_data.to` | date |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /applications/:appId/metrics/data.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-metric-timeslice-data.md) for the provider-specific parameters and requirements.

