# Zeo Route Planner: Create Pickup Delivery Route

Creates a pickup delivery route in Zeo Route Planner.

```
POST https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-pickup-delivery-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-pickup-delivery-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driverId": 1,
  "endAddress": "string",
  "endLatitude": 1,
  "endLongitude": 1,
  "routeName": "Ava Chen",
  "startAddress": "string",
  "startLatitude": 1,
  "startLongitude": 1,
  "stops[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-pickup-delivery-route', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driverId": 1,
    "endAddress": "string",
    "endLatitude": 1,
    "endLongitude": 1,
    "routeName": "Ava Chen",
    "startAddress": "string",
    "startLatitude": 1,
    "startLongitude": 1,
    "stops[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driverId` | number | yes | Driver id for the pickup delivery route. |
| `endAddress` | string | yes | Route end address. |
| `endLatitude` | number | yes | End latitude when provided. |
| `endLongitude` | number | yes | End longitude when provided. |
| `routeName` | string | yes | Route name. |
| `startAddress` | string | yes | Address where the route starts. |
| `startLatitude` | number | yes | Starting latitude when provided. |
| `startLongitude` | number | yes | Starting longitude when provided. |
| `stops[]` | array<object> | yes | Pickup and delivery stops as an array of objects. |

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

Through the native Zeo Route Planner API, this operation is `POST /api/v6/routes` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pickup-delivery-route.md) for the provider-specific parameters and requirements.

