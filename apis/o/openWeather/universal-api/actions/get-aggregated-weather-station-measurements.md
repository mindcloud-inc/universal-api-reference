# OpenWeather: Get Aggregated Weather Station Measurements

Retrieves aggregated weather station measurements from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-aggregated-weather-station-measurements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-aggregated-weather-station-measurements?connectionId=$CONNECTION_ID&stationIds=string&type=string&from=1&to=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stationIds": "string",
  "type": "string",
  "from": "1",
  "to": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-aggregated-weather-station-measurements?${params}`, {
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
| `stationIds` | string | yes | One or more station identifiers to filter measurements for. |
| `type` | string | yes | Aggregation type: hour, day, or month depending on provider support. |
| `from` | number | yes | Unix timestamp for the start of the aggregation window. |
| `to` | number | yes | Unix timestamp for the end of the aggregation window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": 1,
      "humidity": 1,
      "pressure": 1,
      "station_id": "string",
      "temp": 1,
      "type": "string",
      "wind": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | number |  |
| `humidity` | number |  |
| `pressure` | number |  |
| `station_id` | string |  |
| `temp` | number |  |
| `type` | string |  |
| `wind` | number |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/3.0/measurements` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregated-weather-station-measurements.md) for the provider-specific parameters and requirements.

