# Open-Elevation: Look Up Elevations From Body

Retrieves elevations from Open-Elevation for coordinates in the request body.

```
GET https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevations-from-body
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open-Elevation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevations-from-body?connectionId=$CONNECTION_ID&locations%5B%5D=%5Bobject%20Object%5D&locations%5B%5D.latitude=41.161758&locations%5B%5D.longitude=-8.583933" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locations[]": "[object Object]",
  "locations[].latitude": "41.161758",
  "locations[].longitude": "-8.583933"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevations-from-body?${params}`, {
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
| `locations[]` | array<object> | yes | Array of location objects. Each object must include latitude and longitude. Example: `[object Object]`. |
| `locations[].latitude` | number | yes | Latitude for each location in WGS84 decimal degrees. Example: `41.161758`. |
| `locations[].longitude` | number | yes | Longitude for each location in WGS84 decimal degrees. Example: `-8.583933`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elevation": 1,
      "latitude": 1,
      "longitude": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elevation` | number | Elevation in meters. |
| `latitude` | number | Latitude of the requested coordinate. |
| `longitude` | number | Longitude of the requested coordinate. |

## Native endpoint

Through the native Open-Elevation API, this operation is `POST /api/v1/lookup` (base URL `https://api.open-elevation.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/look-up-elevations-from-body.md) for the provider-specific parameters and requirements.

