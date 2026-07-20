# Golemio API: List Parking Locations

Finds parking locations in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-locations?${params}`, {
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
          "capacity": 1,
          "centroid": {},
          "covered": true,
          "hasOccupancyInfo": true,
          "id": "string",
          "lastModifiedAtSource": "2026-05-07T12:00:00.000Z",
          "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "openingHours": [
            {}
          ],
          "parkingPolicy": "string",
          "parkingProhibitions": {},
          "parkingType": "string",
          "payment": {},
          "primarySource": "string",
          "primarySourceId": "string",
          "reservation": {},
          "tariff": "string",
          "validFrom": "2026-05-07T12:00:00.000Z"
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
| `features` | array<object> | Parking location features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<array> | Geometry coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Parking location properties. |
| `features.properties.capacity` | number | Parking capacity. |
| `features.properties.centroid` | object | Location centroid. |
| `features.properties.covered` | boolean | Whether the parking area is covered. |
| `features.properties.hasOccupancyInfo` | boolean | Whether occupancy data is available. |
| `features.properties.id` | string | Parking location identifier. |
| `features.properties.lastModifiedAtSource` | date | Last source modification time. |
| `features.properties.lastUpdatedAt` | date | Last update time. |
| `features.properties.name` | string | Parking location name. |
| `features.properties.openingHours` | array<object> | Opening-hour rules. |
| `features.properties.parkingPolicy` | string | Parking policy. |
| `features.properties.parkingProhibitions` | object | Parking prohibition flags. |
| `features.properties.parkingType` | string | Parking type. |
| `features.properties.payment` | object | Payment links and metadata. |
| `features.properties.primarySource` | string | Source system. |
| `features.properties.primarySourceId` | string | Source-specific identifier. |
| `features.properties.reservation` | object | Reservation metadata. |
| `features.properties.tariff` | string | Related tariff identifier. |
| `features.properties.validFrom` | date | Start of validity. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v3/parking` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-parking-locations.md) for the provider-specific parameters and requirements.

