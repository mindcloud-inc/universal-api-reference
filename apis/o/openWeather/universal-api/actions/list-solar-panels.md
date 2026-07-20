# OpenWeather: List Solar Panels

Lists solar panels in OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-solar-panels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-solar-panels?connectionId=$CONNECTION_ID&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-solar-panels?${params}`, {
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
| `locationId` | string | yes | Solar location identifier. |

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

Through the native OpenWeather API, this operation is `GET https://api.openweathermap.org/energy/2.0/location/:locationId/panels` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-solar-panels.md) for the provider-specific parameters and requirements.

