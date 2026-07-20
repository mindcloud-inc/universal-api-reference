# OpenWeather: Create Solar Panel

Creates a solar panel in OpenWeather.

```
POST https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-panel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-panel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": "string",
  "type": "string",
  "area": 1,
  "tilt": 1,
  "azimuth": 1,
  "peakPower": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-panel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": "string",
    "type": "string",
    "area": 1,
    "tilt": 1,
    "azimuth": 1,
    "peakPower": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | string | yes | Solar location identifier. |
| `type` | string | yes | Solar panel type. |
| `area` | number | yes | Panel area in square meters. |
| `tilt` | number | yes | Panel tilt in degrees. |
| `azimuth` | number | yes | Panel azimuth in degrees. |
| `peakPower` | number | yes | Peak power in kilowatts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "area": 1,
      "azimuth": 1,
      "location_id": "string",
      "panel_id": "string",
      "peak_power": 1,
      "tilt": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `area` | number |  |
| `azimuth` | number |  |
| `location_id` | string |  |
| `panel_id` | string |  |
| `peak_power` | number |  |
| `tilt` | number |  |
| `type` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `POST https://api.openweathermap.org/energy/2.0/location/:locationId/panels` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-solar-panel.md) for the provider-specific parameters and requirements.

