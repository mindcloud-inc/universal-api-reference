# Veterans Affairs Facilities: Find Nearby Facilities by Coordinates

Finds nearby VA facilities by coordinates and drive time.

```
GET https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/find-nearby-facilities-by-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veterans Affairs Facilities `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/find-nearby-facilities-by-coordinates?connectionId=$CONNECTION_ID&limit=25&offset=0&lat=1&long=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "lat": "1",
  "long": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/find-nearby-facilities-by-coordinates?${params}`, {
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
| `lat` | number | yes | Latitude in WGS84 decimal degrees. |
| `long` | number | yes | Longitude in WGS84 decimal degrees. Current VA sandbox runtime expects the query key long. |
| `driveTime` | list | no | Maximum drive time in minutes. One of: `10`, `20`, `30`, `40`, `50`, `60`, `70`, `80`, `90`. Default: `30`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `services[]` | array<string> | no | Optional VA service identifiers to filter by. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "maxTime": 1,
        "minTime": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.maxTime` | number | Upper end of the matching drive-time band in minutes. |
| `attributes.minTime` | number | Lower end of the matching drive-time band in minutes. |
| `id` | string | VA facility ID. |
| `type` | string | JSON API resource type. |

## Native endpoint

Through the native Veterans Affairs Facilities API, this operation is `GET /nearby` (base URL `https://sandbox-api.va.gov/services/va_facilities/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-nearby-facilities-by-coordinates.md) for the provider-specific parameters and requirements.

