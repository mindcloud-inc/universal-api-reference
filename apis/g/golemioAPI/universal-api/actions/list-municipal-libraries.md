# Golemio API: List Municipal Libraries

Finds municipal libraries in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-municipal-libraries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-municipal-libraries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-municipal-libraries?${params}`, {
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
          "district": "string",
          "email": "ava@example.com",
          "id": 1,
          "name": "Ava Chen",
          "openingHours": [
            {}
          ],
          "services": [
            {}
          ],
          "telephone": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "web": "https://example.com"
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
| `features` | array<object> | Municipal library features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<number> | Point coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Library properties. |
| `features.properties.address` | object | Address details. |
| `features.properties.district` | string | Prague district. |
| `features.properties.email` | string | Library email. |
| `features.properties.id` | number | Library identifier. |
| `features.properties.name` | string | Library name. |
| `features.properties.openingHours` | array<object> | Opening hours. |
| `features.properties.services` | array<object> | Available services. |
| `features.properties.telephone` | string | Library phone number. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.properties.web` | string | Library website. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/municipallibraries` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-municipal-libraries.md) for the provider-specific parameters and requirements.

