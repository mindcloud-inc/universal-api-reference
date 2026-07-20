# ChartMogul: Retrieve All Key Metrics

Retrieves all key metrics from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/retrieve-all-key-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/retrieve-all-key-metrics?connectionId=$CONNECTION_ID&endDate=2026-03-01&startDate=2026-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-03-01",
  "startDate": "2026-01-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/retrieve-all-key-metrics?${params}`, {
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
| `endDate` | string | yes | The end date for the metrics range in YYYY-MM-DD format. Example: `2026-03-01`. |
| `interval` | string | no | The reporting interval. Use values like day, week, month, quarter, or year. |
| `startDate` | string | yes | The start date for the metrics range in YYYY-MM-DD format. Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arpa": 1,
      "arpaPercentageChange": 1,
      "arr": 1,
      "arrPercentageChange": 1,
      "asp": 1,
      "aspPercentageChange": 1,
      "customerChurnRate": 1,
      "customerChurnRatePercentageChange": 1,
      "customers": 1,
      "customersPercentageChange": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "ltv": 1,
      "ltvPercentageChange": 1,
      "mrr": 1,
      "mrrChurnRate": 1,
      "mrrChurnRatePercentageChange": 1,
      "mrrPercentageChange": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arpa` | number |  |
| `arpaPercentageChange` | number |  |
| `arr` | number |  |
| `arrPercentageChange` | number |  |
| `asp` | number |  |
| `aspPercentageChange` | number |  |
| `customerChurnRate` | number |  |
| `customerChurnRatePercentageChange` | number |  |
| `customers` | number |  |
| `customersPercentageChange` | number |  |
| `date` | date |  |
| `ltv` | number |  |
| `ltvPercentageChange` | number |  |
| `mrr` | number |  |
| `mrrChurnRate` | number |  |
| `mrrChurnRatePercentageChange` | number |  |
| `mrrPercentageChange` | number |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /metrics/all` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-all-key-metrics.md) for the provider-specific parameters and requirements.

