# Golemio API: List City Districts

Finds city districts in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-city-districts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-city-districts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-city-districts?${params}`, {
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
            [
              "string"
            ]
          ],
          "type": "string"
        },
        "properties": {
          "id": 1,
          "name": "Ava Chen",
          "slug": "string",
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
| `features` | array<object> | City district features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<array> | Polygon coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | District properties. |
| `features.properties.id` | number | District identifier. |
| `features.properties.name` | string | District name. |
| `features.properties.slug` | string | District slug. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/citydistricts` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-city-districts.md) for the provider-specific parameters and requirements.

