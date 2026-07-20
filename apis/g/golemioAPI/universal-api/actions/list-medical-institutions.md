# Golemio API: List Medical Institutions

Finds medical institutions in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-medical-institutions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-medical-institutions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-medical-institutions?${params}`, {
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
          "email": [
            "ava@example.com"
          ],
          "id": "string",
          "institutionCode": "string",
          "name": "Ava Chen",
          "openingHours": [
            {}
          ],
          "pharmacyCode": "string",
          "telephone": [
            "string"
          ],
          "type": {},
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "web": [
            "string"
          ]
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
| `features` | array<object> | Medical institution features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<number> | Point coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Institution properties. |
| `features.properties.address` | object | Address details. |
| `features.properties.district` | string | Prague district. |
| `features.properties.email` | array<string> | Email addresses. |
| `features.properties.id` | string | Institution identifier. |
| `features.properties.institutionCode` | string | Institution code. |
| `features.properties.name` | string | Institution name. |
| `features.properties.openingHours` | array<object> | Opening hours. |
| `features.properties.pharmacyCode` | string | Pharmacy code when applicable. |
| `features.properties.telephone` | array<string> | Phone numbers. |
| `features.properties.type` | object | Institution type. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.properties.web` | array<string> | Web links. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/medicalinstitutions` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-medical-institutions.md) for the provider-specific parameters and requirements.

