# OpenWeather: Create Weather Station

Creates a weather station in your OpenWeather account.

```
POST https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-weather-station
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-weather-station" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string",
  "name": "Ava Chen",
  "latitude": 1,
  "longitude": 1,
  "altitude": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-weather-station', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string",
    "name": "Ava Chen",
    "latitude": 1,
    "longitude": 1,
    "altitude": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | External identifier for the station. |
| `name` | string | yes | Station display name. |
| `latitude` | number | yes | Station latitude. |
| `longitude` | number | yes | Station longitude. |
| `altitude` | number | yes | Station altitude in meters. |

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

Through the native OpenWeather API, this operation is `POST /data/3.0/stations` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-weather-station.md) for the provider-specific parameters and requirements.

