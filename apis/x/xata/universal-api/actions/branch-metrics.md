# Xata: Retrieve branch metrics



```
POST https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-metrics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z",
  "metric": "string",
  "instances[]": [
    "string"
  ],
  "aggregations[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-metrics', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string",
    "branchID": "string",
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z",
    "metric": "string",
    "instances[]": ["string"],
    "aggregations[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes |  |
| `projectID` | string | yes |  |
| `branchID` | string | yes |  |
| `start` | date | yes | Start time |
| `end` | date | yes | End time |
| `metric` | string | yes | Metric name to query |
| `instances[]` | array | yes | List of instance IDs to query |
| `aggregations[]` | array | yes | List of aggregations to get, this is how the data-points within the interval are aggregated. Each one will generate a separate time-series in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "metric": "string",
      "series": [
        {}
      ],
      "start": "2026-05-07T12:00:00.000Z",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `metric` | string |  |
| `series` | array<object> |  |
| `start` | date |  |
| `unit` | string | The unit of the metric (percentage, bytes, ms, etc.) |

## Native endpoint

Through the native Xata API, this operation is `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/metrics` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/branch-metrics.md) for the provider-specific parameters and requirements.

