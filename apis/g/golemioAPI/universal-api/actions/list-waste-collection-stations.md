# Golemio API: List Waste Collection Stations

Finds waste collection stations in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-waste-collection-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-waste-collection-stations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-waste-collection-stations?${params}`, {
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
          "accessibility": {},
          "containers": {
            "cleaningFrequency": {},
            "containerId": 1,
            "containerType": "string",
            "isMonitored": true,
            "lastMeasurement": {},
            "trashType": {}
          },
          "district": "string",
          "id": 1,
          "isMonitored": true,
          "ksnkoId": 1,
          "name": "Ava Chen",
          "stationNumber": "string",
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
| `features` | array<object> | Waste collection station features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<number> | Point coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Station properties. |
| `features.properties.accessibility` | object | Accessibility details. |
| `features.properties.containers` | array<object> | Containers at the station. |
| `features.properties.containers.cleaningFrequency` | object | Cleaning frequency details. |
| `features.properties.containers.containerId` | number | Container identifier. |
| `features.properties.containers.containerType` | string | Container type. |
| `features.properties.containers.isMonitored` | boolean | Whether the container is monitored. |
| `features.properties.containers.lastMeasurement` | object | Latest fullness measurement when monitored. |
| `features.properties.containers.trashType` | object | Trash type details. |
| `features.properties.district` | string | Prague district. |
| `features.properties.id` | number | Station identifier. |
| `features.properties.isMonitored` | boolean | Whether any container is monitored. |
| `features.properties.ksnkoId` | number | KSNKO identifier. |
| `features.properties.name` | string | Station name. |
| `features.properties.stationNumber` | string | Waste station number. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/sortedwastestations` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-waste-collection-stations.md) for the provider-specific parameters and requirements.

