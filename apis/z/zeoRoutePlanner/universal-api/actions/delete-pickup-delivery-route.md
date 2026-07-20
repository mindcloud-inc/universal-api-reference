# Zeo Route Planner: Delete Pickup Delivery Route

Deletes a pickup delivery route from Zeo Route Planner.

```
DELETE https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/delete-pickup-delivery-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/delete-pickup-delivery-route?connectionId=$CONNECTION_ID&driverId=1&routeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driverId": "1",
  "routeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/delete-pickup-delivery-route?${params}`, {
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
| `driverId` | number | yes | Driver id of the pickup delivery route. |
| `routeId` | number | yes | Pickup delivery route id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeo Route Planner API returns.

## Native endpoint

Through the native Zeo Route Planner API, this operation is `DELETE /api/v6/routes/:route_id` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pickup-delivery-route.md) for the provider-specific parameters and requirements.

