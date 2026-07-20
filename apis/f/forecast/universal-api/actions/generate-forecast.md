# Forecast: Generate Forecast

Generates forecasts in Forecast.

```
GET https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-forecast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Forecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-forecast?connectionId=$CONNECTION_ID&identifier=SKU-12345&data=%5Bobject%20Object%5D&periods=6&frequency=M&data%5B%5D.date=2024-01-01&data%5B%5D.value=120" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "SKU-12345",
  "data": "[object Object]",
  "periods": "6",
  "frequency": "M",
  "data[].date": "2024-01-01",
  "data[].value": "120"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-forecast?${params}`, {
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
| `identifier` | string | yes | Unique identifier for the data series, such as a SKU or product ID. Default: `SKU-12345`. |
| `data` | list<object> | yes | Time series datapoints to forecast from. |
| `periods` | number | yes | Number of forecast periods to generate. Default: `6`. |
| `frequency` | string | yes | Data frequency: D, W, M, Q, Y, or H. Default: `M`. |
| `dataType` | string | no | Optional data type for optimized model selection. Default: `sales`. |
| `confidenceLevel` | number | no | Optional confidence level for forecast intervals. Default: `0.95`. |
| `data[].date` | string | yes | Date for one datapoint in YYYY-MM-DD format, for example 2024-01-01. Default: `2024-01-01`. |
| `data[].value` | number | yes | Numeric value for one datapoint. Default: `120`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "forecast": 1,
      "lower": 1,
      "period": 1,
      "upper": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Forecasted date for the period. |
| `forecast` | number | Predicted value for the forecast period. |
| `lower` | number | Lower confidence bound for the forecast. |
| `period` | number | Relative forecast period index. |
| `upper` | number | Upper confidence bound for the forecast. |

## Native endpoint

Through the native Forecast API, this operation is `POST /forecast` (base URL `https://forecastapi.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-forecast.md) for the provider-specific parameters and requirements.

