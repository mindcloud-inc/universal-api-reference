# SimpliRoute: Create Vehicle

Creates a new vehicle in SimpliRoute.

```
POST https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/create-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/create-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "capacity": 1,
  "locationEndAddress": "string",
  "locationEndLatitude": 1,
  "locationEndLongitude": 1,
  "locationStartAddress": "string",
  "locationStartLatitude": 1,
  "locationStartLongitude": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/create-vehicle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "capacity": 1,
    "locationEndAddress": "string",
    "locationEndLatitude": 1,
    "locationEndLongitude": 1,
    "locationStartAddress": "string",
    "locationStartLatitude": 1,
    "locationStartLongitude": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capacity` | number | yes | Vehicle capacity. |
| `defaultDriver` | number | no | Optional default driver ID. |
| `licensePlate` | string | no | Optional license plate. |
| `locationEndAddress` | string | yes | Ending address for the vehicle. |
| `locationEndLatitude` | number | yes | Latitude for the ending address. |
| `locationEndLongitude` | number | yes | Longitude for the ending address. |
| `locationStartAddress` | string | yes | Starting address for the vehicle. |
| `locationStartLatitude` | number | yes | Latitude for the starting address. |
| `locationStartLongitude` | number | yes | Longitude for the starting address. |
| `name` | string | yes | Vehicle name. |
| `referenceId` | string | no | Optional external reference for the vehicle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "capacity_2": 1,
      "capacity_3": 1,
      "capacity_4": 1,
      "codrivers": [
        1
      ],
      "color": "string",
      "cost": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "default_driver": 1,
      "deleted": true,
      "id": 1,
      "license_plate": "string",
      "location_end_address": "string",
      "location_end_latitude": "string",
      "location_end_longitude": "string",
      "location_start_address": "string",
      "location_start_latitude": "string",
      "location_start_longitude": "string",
      "max_number_of_routes": 1,
      "max_route_distance": 1,
      "max_time": "string",
      "max_visit": 1,
      "min_load": 1,
      "min_load_2": 1,
      "min_load_3": 1,
      "min_load_4": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plan": "string",
      "reference_id": "string",
      "rest_time_duration": "string",
      "rest_time_end": "string",
      "rest_time_start": "string",
      "shift_end": "string",
      "shift_start": "string",
      "skills": [
        "string"
      ],
      "status": "string",
      "type_load": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `capacity_2` | number |  |
| `capacity_3` | number |  |
| `capacity_4` | number |  |
| `codrivers` | array<number> |  |
| `color` | string |  |
| `cost` | number |  |
| `created` | date |  |
| `default_driver` | number |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `license_plate` | string |  |
| `location_end_address` | string |  |
| `location_end_latitude` | string |  |
| `location_end_longitude` | string |  |
| `location_start_address` | string |  |
| `location_start_latitude` | string |  |
| `location_start_longitude` | string |  |
| `max_number_of_routes` | number |  |
| `max_route_distance` | number |  |
| `max_time` | string |  |
| `max_visit` | number |  |
| `min_load` | number |  |
| `min_load_2` | number |  |
| `min_load_3` | number |  |
| `min_load_4` | number |  |
| `modified` | date |  |
| `name` | string |  |
| `plan` | string |  |
| `reference_id` | string |  |
| `rest_time_duration` | string |  |
| `rest_time_end` | string |  |
| `rest_time_start` | string |  |
| `shift_end` | string |  |
| `shift_start` | string |  |
| `skills` | array<string> |  |
| `status` | string |  |
| `type_load` | string |  |

## Native endpoint

Through the native SimpliRoute API, this operation is `POST /v1/routes/vehicles/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vehicle.md) for the provider-specific parameters and requirements.

