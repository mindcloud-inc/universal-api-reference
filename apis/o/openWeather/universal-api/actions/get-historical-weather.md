# OpenWeather: Get Historical Weather

Retrieves historical weather data from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-historical-weather
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-historical-weather?connectionId=$CONNECTION_ID&lat=1&lon=1&type=string&start=1&end=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1",
  "type": "string",
  "start": "1",
  "end": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-historical-weather?${params}`, {
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
| `type` | string | yes | Provider history query type. |
| `start` | number | yes | Unix timestamp for the start of the requested history window. |
| `end` | number | yes | Unix timestamp for the end of the requested history window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calctime": 1,
      "city_id": 1,
      "cnt": 1,
      "cod": "string",
      "list": [
        {}
      ],
      "message": "string"
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
| `cnt` | number |  |
| `cod` | string |  |
| `list` | array<object> |  |
| `message` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://history.openweathermap.org/data/2.5/history/city` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-weather.md) for the provider-specific parameters and requirements.

