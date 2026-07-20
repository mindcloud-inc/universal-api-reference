# Open-Elevation: Look Up Elevation

Retrieves elevations from Open-Elevation for coordinates in the query string.

```
GET https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open-Elevation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevation?connectionId=$CONNECTION_ID&locations=41.161758%2C-8.583933" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locations": "41.161758,-8.583933"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevation?${params}`, {
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
| `locations` | string | yes | Latitude,longitude pairs separated by \|, for example 41.161758,-8.583933 or 10,10\|20,20. Example: `41.161758,-8.583933`. |

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

Through the native Open-Elevation API, this operation is `GET /api/v1/lookup` (base URL `https://api.open-elevation.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/look-up-elevation.md) for the provider-specific parameters and requirements.

