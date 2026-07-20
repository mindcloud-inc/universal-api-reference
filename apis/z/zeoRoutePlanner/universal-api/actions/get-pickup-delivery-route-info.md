# Zeo Route Planner: Get Pickup Delivery Route Info

Retrieves pickup delivery route details from Zeo Route Planner.

```
GET https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/get-pickup-delivery-route-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/get-pickup-delivery-route-info?connectionId=$CONNECTION_ID&driverId=1&routeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driverId": "1",
  "routeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/get-pickup-delivery-route-info?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endAddress": "string",
      "endLatitude": 1,
      "endLongitude": 1,
      "id": 1,
      "routeName": "Ava Chen",
      "routeStops": [
        {}
      ],
      "startAddress": "string",
      "startLatitude": 1,
      "startLongitude": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Route creation timestamp. |
| `endAddress` | string | Route end address. |
| `endLatitude` | number | End latitude. |
| `endLongitude` | number | End longitude. |
| `id` | number | Pickup delivery route identifier. |
| `routeName` | string | Pickup delivery route name. |
| `routeStops` | array<object> | Pickup and delivery stops included in the route. |
| `startAddress` | string | Route start address. |
| `startLatitude` | number | Start latitude. |
| `startLongitude` | number | Start longitude. |

## Native endpoint

Through the native Zeo Route Planner API, this operation is `GET /api/v6/routes/:route_id` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pickup-delivery-route-info.md) for the provider-specific parameters and requirements.

