# OpenWeather: Update Weather Station

Updates a weather station in your OpenWeather account.

```
PUT https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/update-weather-station
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/update-weather-station" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/update-weather-station', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stationId` | string | yes | Internal weather station identifier. |
| `externalId` | string | no | Updated external identifier for the station. |
| `name` | string | no | Updated station display name. |
| `latitude` | number | no | Updated station latitude. |
| `longitude` | number | no | Updated station longitude. |
| `altitude` | number | no | Updated station altitude in meters. |

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

Through the native OpenWeather API, this operation is `PUT /data/3.0/stations/:stationId` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-weather-station.md) for the provider-specific parameters and requirements.

