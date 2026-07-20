# Golemio API: List Gardens

Finds gardens in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-gardens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-gardens?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-gardens?${params}`, {
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
          "address": {},
          "description": "string",
          "district": "string",
          "id": "string",
          "image": {},
          "name": "Ava Chen",
          "properties": [
            {}
          ],
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
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
| `features` | array<object> | Garden features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<number> | Point coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Garden properties. |
| `features.properties.address` | object | Address details. |
| `features.properties.description` | string | Garden description. |
| `features.properties.district` | string | Prague district. |
| `features.properties.id` | string | Garden identifier. |
| `features.properties.image` | object | Image metadata. |
| `features.properties.name` | string | Garden name. |
| `features.properties.properties` | array<object> | Additional garden attributes. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.properties.url` | string | Public garden URL returned by Golemio. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/gardens` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-gardens.md) for the provider-specific parameters and requirements.

