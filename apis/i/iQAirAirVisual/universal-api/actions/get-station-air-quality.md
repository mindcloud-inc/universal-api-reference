# IQAir AirVisual: Get Station Air Quality



```
GET https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-station-air-quality
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IQAir AirVisual `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-station-air-quality?connectionId=$CONNECTION_ID&station=Gangnam-gu&city=Seoul&state=Seoul&country=South%20Korea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "station": "Gangnam-gu",
  "city": "Seoul",
  "state": "Seoul",
  "country": "South Korea"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/get-station-air-quality?${params}`, {
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
| `station` | string | yes | Station name exactly as returned by the List Stations action. Example: `Gangnam-gu`. |
| `city` | string | yes | City name containing the requested station. Example: `Seoul`. |
| `state` | string | yes | State name containing the requested station. Example: `Seoul`. |
| `country` | string | yes | Country name containing the requested station. Example: `South Korea`. |

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
          "o3": {
            "aqicn": 1,
            "aqius": 1,
            "conc": 1
          },
          "p1": {
            "aqicn": 1,
            "aqius": 1,
            "conc": 1
          },
          "p2": {
            "aqicn": 1,
            "aqius": 1,
            "conc": 1
          },
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
      "name": "Ava Chen",
      "state": "string",
      "units": {
        "co": "string",
        "n2": "string",
        "o3": "string",
        "p1": "string",
        "p2": "string",
        "pm10": "string",
        "pm25": "string",
        "s2": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City containing the station. |
| `country` | string | Country containing the station. |
| `current` | object | Current observation payload. |
| `current.pollution` | object | Current pollution measurements. |
| `current.pollution.aqicn` | number | China AQI value. |
| `current.pollution.aqius` | number | US AQI value. |
| `current.pollution.maincn` | string | Dominant China pollutant code. |
| `current.pollution.mainus` | string | Dominant US pollutant code. |
| `current.pollution.o3` | object | Ozone pollutant breakdown. |
| `current.pollution.o3.aqicn` | number | Ozone China AQI contribution. |
| `current.pollution.o3.aqius` | number | Ozone US AQI contribution. |
| `current.pollution.o3.conc` | number | Ozone concentration. |
| `current.pollution.p1` | object | PM10 pollutant breakdown. |
| `current.pollution.p1.aqicn` | number | PM10 China AQI contribution. |
| `current.pollution.p1.aqius` | number | PM10 US AQI contribution. |
| `current.pollution.p1.conc` | number | PM10 concentration. |
| `current.pollution.p2` | object | PM2.5 pollutant breakdown. |
| `current.pollution.p2.aqicn` | number | PM2.5 China AQI contribution. |
| `current.pollution.p2.aqius` | number | PM2.5 US AQI contribution. |
| `current.pollution.p2.conc` | number | PM2.5 concentration. |
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
| `location` | object | Geospatial location payload for the station. |
| `location.coordinates` | array<number> | Longitude and latitude coordinates in GeoJSON order. |
| `location.type` | string | GeoJSON geometry type. |
| `name` | string | Station display name. |
| `state` | string | State containing the station. |
| `units` | object | Measurement unit codes for pollutant families. |
| `units.co` | string | Unit code for carbon monoxide. |
| `units.n2` | string | Unit code for nitrogen dioxide. |
| `units.o3` | string | Unit code for ozone. |
| `units.p1` | string | Unit code for PM10. |
| `units.p2` | string | Unit code for PM2.5. |
| `units.pm10` | string | Unit code for PM10 alias. |
| `units.pm25` | string | Unit code for PM2.5 alias. |
| `units.s2` | string | Unit code for sulfur dioxide. |

## Native endpoint

Through the native IQAir AirVisual API, this operation is `GET /v2/station` (base URL `https://api.airvisual.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-station-air-quality.md) for the provider-specific parameters and requirements.

