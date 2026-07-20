# IQAir AirVisual: Get Nearest City Air Quality By IP



```
GET https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-nearest-city-air-quality-by-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IQAir AirVisual `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-nearest-city-air-quality-by-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-nearest-city-air-quality-by-ip?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "current": {
        "pollution": {
          "aqicn": 1,
          "aqius": 1,
          "maincn": "string",
          "mainus": "string",
          "ts": "string"
        },
        "weather": {
          "heatIndex": 1,
          "hu": 1,
          "ic": "string",
          "pr": 1,
          "tp": 1,
          "ts": "string",
          "wd": 1,
          "ws": 1
        }
      },
      "location": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Nearest city name resolved from the caller IP address. |
| `country` | string | Country name for the nearest city. |
| `current` | object | Current observation payload. |
| `current.pollution` | object | Current pollution measurements. |
| `current.pollution.aqicn` | number | China AQI value. |
| `current.pollution.aqius` | number | US AQI value. |
| `current.pollution.maincn` | string | Dominant China pollutant code. |
| `current.pollution.mainus` | string | Dominant US pollutant code. |
| `current.pollution.ts` | string | Timestamp for the pollution reading. |
| `current.weather` | object | Current weather measurements. |
| `current.weather.heatIndex` | number | Calculated heat index in Celsius. |
| `current.weather.hu` | number | Humidity percentage. |
| `current.weather.ic` | string | Weather icon code. |
| `current.weather.pr` | number | Atmospheric pressure in hPa. |
| `current.weather.tp` | number | Temperature in Celsius. |
| `current.weather.ts` | string | Timestamp for the weather reading. |
| `current.weather.wd` | number | Wind direction in degrees. |
| `current.weather.ws` | number | Wind speed in meters per second. |
| `location` | object | Geospatial location payload for the nearest city. |
| `location.coordinates` | array<number> | Longitude and latitude coordinates in GeoJSON order. |
| `location.type` | string | GeoJSON geometry type. |
| `state` | string | State name for the nearest city. |

## Native endpoint

Through the native IQAir AirVisual API, this operation is `GET /v2/nearest_city` (base URL `https://api.airvisual.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nearest-city-air-quality-by-ip.md) for the provider-specific parameters and requirements.

