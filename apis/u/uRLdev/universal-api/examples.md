# URL.dev Universal API Examples

These examples use the MindCloud API key and URL.dev connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Weather

Retrieves current weather for coordinates from URL.dev.

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

Example response:

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

See the full [Get Current Weather action reference](actions/get-current-weather.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uRLdev/latest/actions/get-current-weather).
