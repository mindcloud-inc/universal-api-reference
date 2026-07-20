# OpenWeather: Get Fire Weather Index

Retrieves the fire weather index from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-fire-weather-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-fire-weather-index?connectionId=$CONNECTION_ID&lat=string&lon=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "string",
  "lon": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-fire-weather-index?${params}`, {
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
| `lat` | string | yes | Latitude of the location. |
| `lon` | string | yes | Longitude of the location. |

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

Through the native OpenWeather API, this operation is `GET https://api.openweathermap.org/data/2.5/fwi` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fire-weather-index.md) for the provider-specific parameters and requirements.

