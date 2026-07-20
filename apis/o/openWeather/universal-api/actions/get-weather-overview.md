# OpenWeather: Get Weather Overview

Retrieves an OpenWeather AI weather overview by date.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-weather-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-weather-overview?connectionId=$CONNECTION_ID&lat=1&lon=1&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-weather-overview?${params}`, {
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
| `date` | string | yes | Date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "lat": 1,
      "lon": 1,
      "tz": "string",
      "weather_overview": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `lat` | number |  |
| `lon` | number |  |
| `tz` | string |  |
| `weather_overview` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/3.0/onecall/overview` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weather-overview.md) for the provider-specific parameters and requirements.

