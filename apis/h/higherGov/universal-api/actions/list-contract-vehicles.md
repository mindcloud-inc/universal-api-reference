# HigherGov: List Contract Vehicles

Retrieves contract vehicles from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-contract-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-contract-vehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-contract-vehicles?${params}`, {
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
| `vehicleKey` | string | no | HigherGov Vehicle key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "award_date": "string",
      "last_date_to_order": "string",
      "naics_code": {},
      "path": "string",
      "psc_code": {},
      "shared_ceiling": 1,
      "vehicle_description": "string",
      "vehicle_key": 1,
      "vehicle_name": "Ava Chen",
      "vehicle_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `award_date` | string |  |
| `last_date_to_order` | string |  |
| `naics_code` | object |  |
| `path` | string |  |
| `psc_code` | object |  |
| `shared_ceiling` | number |  |
| `vehicle_description` | string |  |
| `vehicle_key` | number |  |
| `vehicle_name` | string |  |
| `vehicle_type` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/vehicle/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contract-vehicles.md) for the provider-specific parameters and requirements.

