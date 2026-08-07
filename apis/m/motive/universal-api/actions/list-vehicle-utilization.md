# Motive: List vehicle utilization



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-vehicle-utilization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-vehicle-utilization?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-vehicle-utilization?${params}`, {
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
| `vehicleIds` | list<number> | no | Filter utilization by one or more vehicle IDs. Accepts multiple values as an array. |
| `startDate` | date | no | Fetch utilization from this date onward. |
| `endDate` | date | no | Fetch utilization through this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "vehicleIdleRollup": {
        "drivingFuel": 1,
        "drivingTime": 1,
        "idleFuel": 1,
        "idleTime": 1,
        "utilization": 1,
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
| `vehicleIdleRollup.drivingFuel` | number |  |
| `vehicleIdleRollup.drivingTime` | number |  |
| `vehicleIdleRollup.idleFuel` | number |  |
| `vehicleIdleRollup.idleTime` | number |  |
| `vehicleIdleRollup.utilization` | number |  |
| `vehicleIdleRollup.vehicle.id` | number |  |
| `vehicleIdleRollup.vehicle.make` | string |  |
| `vehicleIdleRollup.vehicle.metricUnits` | boolean |  |
| `vehicleIdleRollup.vehicle.model` | string |  |
| `vehicleIdleRollup.vehicle.number` | string |  |
| `vehicleIdleRollup.vehicle.vin` | string |  |
| `vehicleIdleRollup.vehicle.year` | string |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v1/vehicle_utilization` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vehicle-utilization.md) for the provider-specific parameters and requirements.

