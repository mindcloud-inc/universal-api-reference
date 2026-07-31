# Where the ISS at: Get Satellite Position



```
GET https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-satellite-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Where the ISS at `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-satellite-position?connectionId=$CONNECTION_ID&satelliteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "satelliteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-satellite-position?${params}`, {
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
| `satelliteId` | number | yes | NORAD catalog ID; use 25544 for the International Space Station. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `units` | string | no | Optional distance and velocity units: miles or kilometers; provider defaults to kilometers. |
| `timestamp` | number | no | Optional Unix timestamp for the orbital position; provider defaults to the current timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altitude": 1,
      "daynum": 1,
      "footprint": 1,
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "solar_lat": 1,
      "solar_lon": 1,
      "timestamp": 1,
      "units": "string",
      "velocity": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altitude` | number | Altitude in the requested units. |
| `daynum` | number | Julian day number. |
| `footprint` | number | Ground footprint in the requested units. |
| `id` | number | NORAD catalog ID. |
| `latitude` | number | Latitude in decimal degrees. |
| `longitude` | number | Longitude in decimal degrees. |
| `name` | string | Satellite name. |
| `solar_lat` | number | Solar latitude. |
| `solar_lon` | number | Solar longitude. |
| `timestamp` | number | Unix timestamp for the position. |
| `units` | string | Units used for altitude, velocity, and footprint. |
| `velocity` | number | Velocity in the requested units. |
| `visibility` | string | Current visibility state. |

## Native endpoint

Through the native Where the ISS at API, this operation is `GET /satellites/:satelliteId` (base URL `https://api.wheretheiss.at/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-satellite-position.md) for the provider-specific parameters and requirements.

