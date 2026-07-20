# OpenWeather: Get Accumulated Precipitation

Retrieves accumulated precipitation data from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-accumulated-precipitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-accumulated-precipitation?connectionId=$CONNECTION_ID&lat=1&lon=1&start=1&end=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1",
  "start": "1",
  "end": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-accumulated-precipitation?${params}`, {
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
| `start` | number | yes | Unix timestamp for the start of accumulation. |
| `end` | number | yes | Unix timestamp for the end of accumulation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "date": 1,
      "precipitation": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `date` | number |  |
| `precipitation` | number |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://history.openweathermap.org/data/2.5/history/accumulated_precipitation` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-accumulated-precipitation.md) for the provider-specific parameters and requirements.

