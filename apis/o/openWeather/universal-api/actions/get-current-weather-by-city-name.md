# OpenWeather: Get Current Weather by City Name

Retrieves current weather from OpenWeather by city name.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather-by-city-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather-by-city-name?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather-by-city-name?${params}`, {
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
| `q` | string | yes | City name, optionally including state code and country code separated by commas. |

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
| `base` | string |  |
| `clouds` | object |  |
| `cod` | number |  |
| `coord` | object |  |
| `dt` | number |  |
| `id` | number |  |
| `main` | object |  |
| `name` | string |  |
| `sys` | object |  |
| `timezone` | number |  |
| `visibility` | number |  |
| `weather` | array<object> |  |
| `wind` | object |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/2.5/weather` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-weather-by-city-name.md) for the provider-specific parameters and requirements.

