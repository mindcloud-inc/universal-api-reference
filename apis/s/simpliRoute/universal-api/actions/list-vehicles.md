# SimpliRoute: List Vehicles

Retrieves vehicles from SimpliRoute.

```
GET https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/list-vehicles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/list-vehicles?${params}`, {
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
| `includeExtraProperties` | boolean | no | When true, include the extraProperties object in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "capacity_2": 1,
      "capacity_3": 1,
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
      "max_time": "string",
      "max_visit": 1,
      "min_load": 1,
      "min_load_2": 1,
      "min_load_3": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "reference_id": "string",
      "rest_time_duration": "string",
      "rest_time_end": "string",
      "rest_time_start": "string",
      "shift_end": "string",
      "shift_start": "string",
      "skills": [
        "string"
      ],
      "status": "string"
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
| `max_time` | string |  |
| `max_visit` | number |  |
| `min_load` | number |  |
| `min_load_2` | number |  |
| `min_load_3` | number |  |
| `modified` | date |  |
| `name` | string |  |
| `reference_id` | string |  |
| `rest_time_duration` | string |  |
| `rest_time_end` | string |  |
| `rest_time_start` | string |  |
| `shift_end` | string |  |
| `shift_start` | string |  |
| `skills` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native SimpliRoute API, this operation is `GET /v1/routes/vehicles/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

