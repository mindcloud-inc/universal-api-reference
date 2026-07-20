# SimpliRoute: Update Vehicle

Updates an existing vehicle in SimpliRoute.

```
PUT https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/update-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/update-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vehicleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/update-vehicle', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vehicleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capacity` | number | no | Optional updated capacity. |
| `licensePlate` | string | no | Optional updated license plate. |
| `name` | string | no | Optional updated vehicle name. |
| `referenceId` | string | no | Optional updated reference ID. |
| `vehicleId` | number | yes | The SimpliRoute vehicle ID. |

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

Through the native SimpliRoute API, this operation is `PATCH /v1/routes/vehicles/:vehicle_id/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vehicle.md) for the provider-specific parameters and requirements.

