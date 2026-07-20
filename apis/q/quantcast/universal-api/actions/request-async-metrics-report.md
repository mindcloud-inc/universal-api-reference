# Quantcast: Request Async Metrics Report

Requests an async metrics report from Quantcast.

```
POST https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/request-async-metrics-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/request-async-metrics-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "metricsReportRequest": "{entity:{type:ACCOUNT,id:9974296},dateRange:{absoluteDateRange:{startDate:\"2026-04-01\",endDate:\"2026-04-07\"},timezone:\"UTC\"},breakdowns:[\"Day\"],metrics:[\"Impressions\"]}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/request-async-metrics-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "metricsReportRequest": "{entity:{type:ACCOUNT,id:9974296},dateRange:{absoluteDateRange:{startDate:\"2026-04-01\",endDate:\"2026-04-07\"},timezone:\"UTC\"},breakdowns:[\"Day\"],metrics:[\"Impressions\"]}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metricsReportRequest` | string | yes | GraphQL input object literal for the async metrics report request. Default: `{entity:{type:ACCOUNT,id:9974296},dateRange:{absoluteDateRange:{startDate:\"2026-04-01\",endDate:\"2026-04-07\"},timezone:\"UTC\"},breakdowns:[\"Day\"],metrics:[\"Impressions\"]}`. |
| `fileName` | string | no | Optional filename for the exported report. Default: `quantcast-metrics-report.csv`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncMetricsReport": {
        "reportRequestId": 1,
        "request": {
          "fileName": "Ava Chen"
        },
        "status": "string",
        "warningMessage": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncMetricsReport` | object | Async metrics report request accepted by Quantcast. |
| `asyncMetricsReport.reportRequestId` | number | Async report request identifier. |
| `asyncMetricsReport.request` | object | Original async report request metadata. |
| `asyncMetricsReport.request.fileName` | string | Requested output file name. |
| `asyncMetricsReport.status` | string | Current status of the async report request. |
| `asyncMetricsReport.warningMessage` | array<string> | Warning messages returned by Quantcast. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-async-metrics-report.md) for the provider-specific parameters and requirements.

