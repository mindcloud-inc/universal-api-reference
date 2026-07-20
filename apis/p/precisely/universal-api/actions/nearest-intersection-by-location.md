# Precisely: Nearest Intersection By Location

Retrieves the nearest intersection from Precisely by location.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearest-intersection-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearest-intersection-by-location?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearest-intersection-by-location?${params}`, {
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
| `latitude` | number | yes | Latitude for the target point. |
| `longitude` | number | yes | Longitude for the target point. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distance": {
        "unit": "string",
        "value": 1
      },
      "driveDistance": {
        "unit": "string",
        "value": 1
      },
      "driveTime": {
        "unit": "string",
        "value": 1
      },
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "roads": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distance.unit` | string | Unit used for the reported distance. |
| `distance.value` | number | Distance from the input point to the nearest intersection. |
| `driveDistance.unit` | string | Unit used for the reported drive distance. |
| `driveDistance.value` | number | Estimated drive distance to the nearest intersection. |
| `driveTime.unit` | string | Unit used for the reported drive time. |
| `driveTime.value` | number | Estimated drive time to the nearest intersection. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates for the matched intersection. |
| `geometry.type` | string | GeoJSON geometry type for the matched intersection. |
| `roads` | array<object> | Road segments that form the nearest intersection. |

## Native endpoint

Through the native Precisely API, this operation is `GET /streets/v1/intersection/bylocation` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nearest-intersection-by-location.md) for the provider-specific parameters and requirements.

