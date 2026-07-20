# OpenWeather: List Weather Stations

Lists weather stations in your OpenWeather account.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-weather-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-weather-stations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-weather-stations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "altitude": 1,
      "external_id": "string",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "rank": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altitude` | number |  |
| `external_id` | string |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `rank` | number |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /data/3.0/stations` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-weather-stations.md) for the provider-specific parameters and requirements.

