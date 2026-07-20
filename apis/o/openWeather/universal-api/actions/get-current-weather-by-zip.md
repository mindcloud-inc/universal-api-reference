# OpenWeather: Get Current Weather by ZIP

Retrieves current weather from OpenWeather by ZIP code.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather-by-zip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather-by-zip?connectionId=$CONNECTION_ID&zip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather-by-zip?${params}`, {
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
| `zip` | string | yes | ZIP code with optional country code, for example 94040,us. |

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

Through the native OpenWeather API, this operation is `GET /data/2.5/weather` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-weather-by-zip.md) for the provider-specific parameters and requirements.

