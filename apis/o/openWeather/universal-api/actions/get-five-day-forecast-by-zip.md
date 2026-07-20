# OpenWeather: Get 5 Day Forecast by ZIP

Retrieves a 5-day forecast from OpenWeather by ZIP code.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-five-day-forecast-by-zip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-five-day-forecast-by-zip?connectionId=$CONNECTION_ID&zip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-five-day-forecast-by-zip?${params}`, {
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
      "city": {},
      "cnt": 1,
      "cod": "string",
      "list": [
        {}
      ],
      "message": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | object |  |
| `cnt` | number |  |
| `cod` | string |  |
| `list` | array<object> |  |
| `message` | number |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/2.5/forecast` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-five-day-forecast-by-zip.md) for the provider-specific parameters and requirements.

