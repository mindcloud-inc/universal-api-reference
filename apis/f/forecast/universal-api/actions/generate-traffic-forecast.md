# Forecast: Generate Traffic Forecast

Generates traffic forecasts in Forecast.

```
GET https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-traffic-forecast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Forecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-traffic-forecast?connectionId=$CONNECTION_ID&identifier=traffic-series-1&data=%5Bobject%20Object%5D&periods=6&frequency=D&trafficSettings.currentCapacity=2200&trafficSettings.baselineTraffic=1500&data%5B%5D.date=2024-01-01&data%5B%5D.value=1200" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "traffic-series-1",
  "data": "[object Object]",
  "periods": "6",
  "frequency": "D",
  "trafficSettings.currentCapacity": "2200",
  "trafficSettings.baselineTraffic": "1500",
  "data[].date": "2024-01-01",
  "data[].value": "1200"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-traffic-forecast?${params}`, {
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
| `identifier` | string | yes | Default: `traffic-series-1`. |
| `data` | list<object> | yes |  |
| `periods` | number | yes | Default: `6`. |
| `frequency` | string | yes | Default: `D`. |
| `trafficSettings.currentCapacity` | number | yes | Default: `2200`. |
| `trafficSettings.baselineTraffic` | number | yes | Default: `1500`. |
| `dataType` | string | no | Default: `traffic`. |
| `confidenceLevel` | number | no | Default: `0.95`. |
| `data[].date` | string | yes | Default: `2024-01-01`. |
| `data[].value` | number | yes | Default: `1200`. |

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
| `date` | date | Forecasted date for the traffic period. |
| `forecast` | number | Predicted traffic value for the forecast period. |
| `lower` | number | Lower confidence bound for the traffic forecast. |
| `period` | number | Relative forecast period index. |
| `upper` | number | Upper confidence bound for the traffic forecast. |

## Native endpoint

Through the native Forecast API, this operation is `POST /traffic-forecasting` (base URL `https://forecastapi.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-traffic-forecast.md) for the provider-specific parameters and requirements.

