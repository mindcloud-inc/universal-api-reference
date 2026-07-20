# Rentman: List Vehicles



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-vehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-vehicles?${params}`, {
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
      "asset_location": "string",
      "cost_rate": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "custom": {},
      "displayname": "Ava Chen",
      "distance_cost": 1,
      "fixed_cost": 1,
      "folder": "string",
      "height": 1,
      "id": 1,
      "image": "string",
      "in_planner": true,
      "inspection_date": "string",
      "length": 1,
      "licenseplate": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "multiple": true,
      "name": "Ava Chen",
      "payload_capacity": 1,
      "remark": "string",
      "seats": 1,
      "surface_area": "string",
      "tags": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset_location` | string |  |
| `cost_rate` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `custom` | object |  |
| `displayname` | string |  |
| `distance_cost` | number |  |
| `fixed_cost` | number |  |
| `folder` | string |  |
| `height` | number |  |
| `id` | number |  |
| `image` | string |  |
| `in_planner` | boolean |  |
| `inspection_date` | string |  |
| `length` | number |  |
| `licenseplate` | string |  |
| `modified` | date |  |
| `multiple` | boolean |  |
| `name` | string |  |
| `payload_capacity` | number |  |
| `remark` | string |  |
| `seats` | number |  |
| `surface_area` | string |  |
| `tags` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /vehicles` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

