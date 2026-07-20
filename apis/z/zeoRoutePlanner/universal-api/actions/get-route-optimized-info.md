# Zeo Route Planner: Get Route Optimized Info

Retrieves optimized route details from Zeo Route Planner.

```
GET https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/get-route-optimized-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/get-route-optimized-info?connectionId=$CONNECTION_ID&driverId=1&routeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driverId": "1",
  "routeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/get-route-optimized-info?${params}`, {
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
| `driverId` | number | yes | Driver id of the route. |
| `routeId` | number | yes | Route id to fetch optimized information for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "legs": [
        {}
      ],
      "optimized": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `legs` | array<object> | Optimized route legs including distance, duration, and stop order details. |
| `optimized` | boolean | Whether the route is optimized. |

## Native endpoint

Through the native Zeo Route Planner API, this operation is `GET /api/v5/routes/:route_id/optimize_route` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-optimized-info.md) for the provider-specific parameters and requirements.

