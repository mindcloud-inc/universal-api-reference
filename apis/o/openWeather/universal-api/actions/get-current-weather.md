# OpenWeather: Get Current Weather

Retrieves current weather from OpenWeather by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather?connectionId=$CONNECTION_ID&lat=1&lon=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather?${params}`, {
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
| `lat` | number | yes | Latitude of the location to fetch weather for. |
| `lon` | number | yes | Longitude of the location to fetch weather for. |
| `units` | string | no | Units to use for temperature and wind speed. One of: `0`, `1`, `2`. |
| `lang` | string | no | Language code for weather condition descriptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "clouds": {},
      "cod": 1,
      "coord": {},
      "dt": 1,
      "id": 1,
      "main": {},
      "name": "Ava Chen",
      "sys": {},
      "timezone": 1,
      "visibility": 1,
      "weather": [
        {}
      ],
      "wind": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | string | Internal parameter for the source of weather data. |
| `clouds` | object | Cloudiness information. |
| `cod` | number | Provider response code. |
| `coord` | object | Coordinates of the requested location. |
| `dt` | number | Time of data calculation as a Unix timestamp. |
| `id` | number | OpenWeather city identifier. |
| `main` | object | Main weather measurements such as temperature and pressure. |
| `name` | string | Resolved city name. |
| `sys` | object | System data about the location and station. |
| `timezone` | number | Shift in seconds from UTC. |
| `visibility` | number | Visibility in meters. |
| `weather` | array<object> | Weather conditions for the location. |
| `wind` | object | Wind measurements. |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/2.5/weather` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-weather.md) for the provider-specific parameters and requirements.

