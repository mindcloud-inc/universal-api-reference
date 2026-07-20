# OpenWeather: Get One Call Time Machine

Retrieves One Call weather from OpenWeather for a timestamp.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-one-call-time-machine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-one-call-time-machine?connectionId=$CONNECTION_ID&lat=1&lon=1&dt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1",
  "dt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-one-call-time-machine?${params}`, {
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
| `dt` | number | yes | Unix timestamp for the historical point in time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "lat": 1,
      "lon": 1,
      "timezone": "string",
      "timezone_offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `lat` | number |  |
| `lon` | number |  |
| `timezone` | string |  |
| `timezone_offset` | number |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/3.0/onecall/timemachine` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-one-call-time-machine.md) for the provider-specific parameters and requirements.

