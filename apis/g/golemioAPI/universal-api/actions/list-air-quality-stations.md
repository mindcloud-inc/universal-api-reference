# Golemio API: List Air Quality Stations

Finds air quality stations in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-stations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-stations?${params}`, {
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
          "district": "string",
          "id": "string",
          "measurement": {
            "AQHourlyIndex": "https://example.com",
            "components": {
              "averagedTime": {
                "averagedHours": "string",
                "value": 1
              },
              "type": "string"
            }
          },
          "name": "Ava Chen",
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
| `features` | array<object> | Air-quality station features. |
| `features.geometry` | object | GeoJSON geometry. |
| `features.geometry.coordinates` | array<number> | Point coordinates. |
| `features.geometry.type` | string | Geometry type. |
| `features.properties` | object | Station properties. |
| `features.properties.district` | string | Prague district. |
| `features.properties.id` | string | Station identifier. |
| `features.properties.measurement` | object | Current air-quality measurement. |
| `features.properties.measurement.AQHourlyIndex` | string | Hourly air-quality index. |
| `features.properties.measurement.components` | array<object> | Measured pollutant components. |
| `features.properties.measurement.components.averagedTime` | object | Averaging window and measured value. |
| `features.properties.measurement.components.averagedTime.averagedHours` | string | Averaging window in hours. |
| `features.properties.measurement.components.averagedTime.value` | number | Measured averaged value. |
| `features.properties.measurement.components.type` | string | Component pollutant type. |
| `features.properties.name` | string | Station name. |
| `features.properties.updatedAt` | date | Last update time. |
| `features.type` | string | GeoJSON feature type. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/airqualitystations` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-air-quality-stations.md) for the provider-specific parameters and requirements.

