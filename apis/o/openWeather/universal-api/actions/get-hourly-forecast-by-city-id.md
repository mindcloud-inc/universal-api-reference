# OpenWeather: Get Hourly Forecast by City ID

Retrieves an hourly forecast from OpenWeather by city ID.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-hourly-forecast-by-city-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-hourly-forecast-by-city-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-hourly-forecast-by-city-id?${params}`, {
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
| `id` | number | yes | OpenWeather city identifier. |

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

Through the native OpenWeather API, this operation is `GET /data/2.5/forecast/hourly` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hourly-forecast-by-city-id.md) for the provider-specific parameters and requirements.

