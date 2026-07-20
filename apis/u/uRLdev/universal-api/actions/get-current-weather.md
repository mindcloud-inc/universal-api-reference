# URL.dev: Get Current Weather

Retrieves current weather for coordinates from URL.dev.

```
GET https://connect.mindcloud.co/v1/universal/uRLdev/latest/actions/get-current-weather
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a URL.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uRLdev/latest/actions/get-current-weather?connectionId=$CONNECTION_ID&latitude=37.7749&longitude=-122.4194" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "37.7749",
  "longitude": "-122.4194"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uRLdev/latest/actions/get-current-weather?${params}`, {
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
| `latitude` | number | yes | Latitude coordinate for the current weather lookup. Default: `37.7749`. |
| `longitude` | number | yes | Longitude coordinate for the current weather lookup. Default: `-122.4194`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current": {
        "apparentTemperature": 1,
        "cloudCover": 1,
        "interval": 1,
        "isDay": 1,
        "precipitation": 1,
        "pressureMsl": 1,
        "rain": 1,
        "relativeHumidity2m": 1,
        "showers": 1,
        "snowfall": 1,
        "surfacePressure": 1,
        "temperature2m": 1,
        "time": "string",
        "weatherCode": 1,
        "weatherDescription": "string",
        "windDirection10m": 1,
        "windGusts10m": 1,
        "windSpeed10m": 1
      },
      "currentUnits": {
        "apparentTemperature": "string",
        "cloudCover": "string",
        "interval": "string",
        "isDay": "string",
        "precipitation": "string",
        "pressureMsl": "string",
        "rain": "string",
        "relativeHumidity2m": "string",
        "showers": "string",
        "snowfall": "string",
        "surfacePressure": "string",
        "temperature2m": "string",
        "time": "string",
        "weatherCode": "string",
        "windDirection10m": "string",
        "windGusts10m": "string",
        "windSpeed10m": "string"
      },
      "elevation": 1,
      "generationtimeMs": 1,
      "latitude": 1,
      "longitude": 1,
      "timezone": "string",
      "timezoneAbbreviation": "string",
      "utcOffsetSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current.apparentTemperature` | number |  |
| `current.cloudCover` | number |  |
| `current.interval` | number |  |
| `current.isDay` | number |  |
| `current.precipitation` | number |  |
| `current.pressureMsl` | number |  |
| `current.rain` | number |  |
| `current.relativeHumidity2m` | number |  |
| `current.showers` | number |  |
| `current.snowfall` | number |  |
| `current.surfacePressure` | number |  |
| `current.temperature2m` | number |  |
| `current.time` | string |  |
| `current.weatherCode` | number |  |
| `current.weatherDescription` | string |  |
| `current.windDirection10m` | number |  |
| `current.windGusts10m` | number |  |
| `current.windSpeed10m` | number |  |
| `currentUnits.apparentTemperature` | string |  |
| `currentUnits.cloudCover` | string |  |
| `currentUnits.interval` | string |  |
| `currentUnits.isDay` | string |  |
| `currentUnits.precipitation` | string |  |
| `currentUnits.pressureMsl` | string |  |
| `currentUnits.rain` | string |  |
| `currentUnits.relativeHumidity2m` | string |  |
| `currentUnits.showers` | string |  |
| `currentUnits.snowfall` | string |  |
| `currentUnits.surfacePressure` | string |  |
| `currentUnits.temperature2m` | string |  |
| `currentUnits.time` | string |  |
| `currentUnits.weatherCode` | string |  |
| `currentUnits.windDirection10m` | string |  |
| `currentUnits.windGusts10m` | string |  |
| `currentUnits.windSpeed10m` | string |  |
| `elevation` | number |  |
| `generationtimeMs` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `timezone` | string |  |
| `timezoneAbbreviation` | string |  |
| `utcOffsetSeconds` | number |  |

## Native endpoint

Through the native URL.dev API, this operation is `GET /current/` (base URL `https://v-20260317--open-meteo--superuser.su.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-weather.md) for the provider-specific parameters and requirements.

