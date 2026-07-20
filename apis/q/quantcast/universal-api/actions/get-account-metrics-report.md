# Quantcast: Get Account Metrics Report

Retrieves an account metrics report from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-account-metrics-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-account-metrics-report?connectionId=$CONNECTION_ID&accountId=9974296&startDate=2026-04-01&endDate=2026-04-07&breakdowns=Day&metrics=Impressions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "9974296",
  "startDate": "2026-04-01",
  "endDate": "2026-04-07",
  "breakdowns": "Day",
  "metrics": "Impressions"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-account-metrics-report?${params}`, {
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
| `accountId` | number | yes | Quantcast account ID to report on. Default: `9974296`. |
| `startDate` | string | yes | Report start date in YYYY-MM-DD format. Default: `2026-04-01`. |
| `endDate` | string | yes | Report end date in YYYY-MM-DD format. Default: `2026-04-07`. |
| `timezone` | string | no | Timezone used to interpret the report range. Default: `UTC`. |
| `breakdowns` | string | yes | Quantcast breakdown display name, for example Day. Default: `Day`. |
| `metrics` | string | yes | Quantcast metric display name, for example Impressions. Default: `Impressions`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountMetricsReport": {
        "breakdowns": {
          "key": "string",
          "value": "string"
        },
        "metadata": [
          {}
        ],
        "metrics": {
          "value": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountMetricsReport` | array<object> | Metrics report rows returned by Quantcast. |
| `accountMetricsReport.breakdowns` | array<object> | Breakdown values for the report row. |
| `accountMetricsReport.breakdowns.key` | string | Breakdown key. |
| `accountMetricsReport.breakdowns.value` | string | Breakdown value. |
| `accountMetricsReport.metadata` | array<object> | Additional metadata for the report row. |
| `accountMetricsReport.metrics` | array<object> | Metric values for the report row. |
| `accountMetricsReport.metrics.value` | string | Metric value. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-metrics-report.md) for the provider-specific parameters and requirements.

