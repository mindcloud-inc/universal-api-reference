# OpenWeather: Get Statistical Weather by Day

Retrieves daily weather statistics from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-statistical-weather-by-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-statistical-weather-by-day?connectionId=$CONNECTION_ID&lat=1&lon=1&month=1&day=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1",
  "month": "1",
  "day": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-statistical-weather-by-day?${params}`, {
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
| `lat` | number | yes | Latitude of the location. |
| `lon` | number | yes | Longitude of the location. |
| `month` | number | yes | Month number for aggregation. |
| `day` | number | yes | Day of month for aggregation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calctime": 1,
      "city_id": 1,
      "cod": "string",
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calctime` | number |  |
| `city_id` | number |  |
| `cod` | string |  |
| `result` | object |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://history.openweathermap.org/data/2.5/aggregated/day` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statistical-weather-by-day.md) for the provider-specific parameters and requirements.

