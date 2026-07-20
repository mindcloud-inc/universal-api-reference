# Pirate Weather: Get Hourly Forecast

Retrieves an hourly forecast from Pirate Weather.

```
GET https://connect.mindcloud.co/v1/universal/pirateWeather/latest/actions/get-hourly-forecast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirate Weather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirateWeather/latest/actions/get-hourly-forecast?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirateWeather/latest/actions/get-hourly-forecast?${params}`, {
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
| `latitude` | number | yes | Latitude in decimal degrees. |
| `longitude` | number | yes | Longitude in decimal degrees. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elevation": 1,
      "flags": {},
      "hourly": {},
      "latitude": 1,
      "longitude": 1,
      "offset": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elevation` | number |  |
| `flags` | object |  |
| `hourly` | object |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `offset` | number |  |
| `timezone` | string |  |

## Native endpoint

Through the native Pirate Weather API, this operation is `GET /forecast/header-auth/:latitude,:longitude` (base URL `https://api.pirateweather.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hourly-forecast.md) for the provider-specific parameters and requirements.

