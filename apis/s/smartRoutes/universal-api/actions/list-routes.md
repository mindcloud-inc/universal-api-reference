# SmartRoutes: List Routes



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-routes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-routes?${params}`, {
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
| `updatedAtMin` | date | no | Minimum updated date and time for filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual_distance": 1,
      "completed_ts": "string",
      "created": "string",
      "date": "string",
      "dispatched": true,
      "distance": 1,
      "id": 1,
      "name": "Ava Chen",
      "operation_time": "string",
      "plan_id": 1,
      "started_timestamp": "string",
      "stops": 1,
      "total_time": "string",
      "travel_time": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual_distance` | number |  |
| `completed_ts` | string |  |
| `created` | string |  |
| `date` | string |  |
| `dispatched` | boolean |  |
| `distance` | number |  |
| `id` | number |  |
| `name` | string |  |
| `operation_time` | string |  |
| `plan_id` | number |  |
| `started_timestamp` | string |  |
| `stops` | number |  |
| `total_time` | string |  |
| `travel_time` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native SmartRoutes API, this operation is `GET /routes` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-routes.md) for the provider-specific parameters and requirements.

