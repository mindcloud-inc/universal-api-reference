# Motive: List driver performance events



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-driver-performance-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-driver-performance-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-driver-performance-events?${params}`, {
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
| `driverIds` | list<number> | no | Filter events by one or more driver IDs. Accepts multiple values as an array. |
| `vehicleIds` | list<number> | no | Filter events by one or more vehicle IDs. Accepts multiple values as an array. |
| `eventTypes` | list<string> | no | Filter events by Motive event type. Accepts multiple values as an array. |
| `startDate` | date | no | Fetch events from this date onward. |
| `endDate` | date | no | Fetch events up to this date. |
| `updatedAfter` | date | no | Return events updated after the given timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "driverPerformanceEvent": {
        "acceleration": 1,
        "coachingStatus": "string",
        "driver": {
          "driverCompanyId": "string",
          "email": {},
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "role": "string",
          "status": "string",
          "username": "Ava Chen"
        },
        "duration": 1,
        "eldDevice": {
          "id": 1,
          "identifier": "string",
          "model": "string"
        },
        "endBearing": 1,
        "endSpeed": 1,
        "endTime": "string",
        "id": 1,
        "intensity": "string",
        "lat": 1,
        "location": "string",
        "lon": 1,
        "mGpsHeading": [
          1
        ],
        "mGpsLat": [
          1
        ],
        "mGpsLon": [
          1
        ],
        "mGpsSpd": [
          1
        ],
        "mVehSpd": [
          1
        ],
        "startBearing": 1,
        "startSpeed": 1,
        "startTime": "string",
        "type": "string",
        "vehicle": {
          "id": 1,
          "make": "string",
          "metricUnits": true,
          "model": "string",
          "number": "string",
          "vin": "string",
          "year": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `driverPerformanceEvent.acceleration` | number |  |
| `driverPerformanceEvent.coachingStatus` | string |  |
| `driverPerformanceEvent.driver.driverCompanyId` | string |  |
| `driverPerformanceEvent.driver.email` | object |  |
| `driverPerformanceEvent.driver.firstName` | string |  |
| `driverPerformanceEvent.driver.id` | number |  |
| `driverPerformanceEvent.driver.lastName` | string |  |
| `driverPerformanceEvent.driver.role` | string |  |
| `driverPerformanceEvent.driver.status` | string |  |
| `driverPerformanceEvent.driver.username` | string |  |
| `driverPerformanceEvent.duration` | number |  |
| `driverPerformanceEvent.eldDevice.id` | number |  |
| `driverPerformanceEvent.eldDevice.identifier` | string |  |
| `driverPerformanceEvent.eldDevice.model` | string |  |
| `driverPerformanceEvent.endBearing` | number |  |
| `driverPerformanceEvent.endSpeed` | number |  |
| `driverPerformanceEvent.endTime` | string |  |
| `driverPerformanceEvent.id` | number |  |
| `driverPerformanceEvent.intensity` | string |  |
| `driverPerformanceEvent.lat` | number |  |
| `driverPerformanceEvent.location` | string |  |
| `driverPerformanceEvent.lon` | number |  |
| `driverPerformanceEvent.mGpsHeading[]` | number |  |
| `driverPerformanceEvent.mGpsLat[]` | number |  |
| `driverPerformanceEvent.mGpsLon[]` | number |  |
| `driverPerformanceEvent.mGpsSpd[]` | number |  |
| `driverPerformanceEvent.mVehSpd[]` | number |  |
| `driverPerformanceEvent.startBearing` | number |  |
| `driverPerformanceEvent.startSpeed` | number |  |
| `driverPerformanceEvent.startTime` | string |  |
| `driverPerformanceEvent.type` | string |  |
| `driverPerformanceEvent.vehicle.id` | number |  |
| `driverPerformanceEvent.vehicle.make` | string |  |
| `driverPerformanceEvent.vehicle.metricUnits` | boolean |  |
| `driverPerformanceEvent.vehicle.model` | string |  |
| `driverPerformanceEvent.vehicle.number` | string |  |
| `driverPerformanceEvent.vehicle.vin` | string |  |
| `driverPerformanceEvent.vehicle.year` | string |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v1/driver_performance_events` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-driver-performance-events.md) for the provider-specific parameters and requirements.

