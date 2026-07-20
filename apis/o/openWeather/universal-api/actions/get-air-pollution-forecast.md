# OpenWeather: Get Air Pollution Forecast

Retrieves an air pollution forecast from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-air-pollution-forecast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-air-pollution-forecast?connectionId=$CONNECTION_ID&lat=1&lon=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-air-pollution-forecast?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "coord": {},
      "list": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coord` | object |  |
| `list` | array<object> |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/2.5/air_pollution/forecast` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-air-pollution-forecast.md) for the provider-specific parameters and requirements.

