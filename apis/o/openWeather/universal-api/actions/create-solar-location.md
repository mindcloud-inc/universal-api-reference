# OpenWeather: Create Solar Location

Creates a solar location in OpenWeather.

```
POST https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "coordinates": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "coordinates": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `coordinates` | object | yes | GeoJSON point coordinates for the solar location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coordinates": {},
      "location_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coordinates` | object |  |
| `location_id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `POST https://api.openweathermap.org/energy/2.0/locations` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-solar-location.md) for the provider-specific parameters and requirements.

