# Golemio API: List Bicycle Counters

Finds bicycle counters in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-bicycle-counters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-bicycle-counters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-bicycle-counters?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "features": {
        "geometry": {
          "coordinates": [
            1
          ],
          "type": "string"
        },
        "properties": {
          "directions": {
            "id": "string",
            "name": "Ava Chen"
          },
          "id": "string",
          "name": "Ava Chen",
          "route": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        },
        "type": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<object> | Bicycle counter features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<number> | Point coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Counter properties. |
| `features.properties.directions` | array<object> | Counted directions. |
| `features.properties.directions.id` | string | Direction identifier. |
| `features.properties.directions.name` | string | Direction name. |
| `features.properties.id` | string | Counter identifier. |
| `features.properties.name` | string | Counter name. |
| `features.properties.route` | string | Route identifier. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/bicyclecounters` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bicycle-counters.md) for the provider-specific parameters and requirements.

