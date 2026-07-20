# Zeo Route Planner: Create Route

Creates a new route in Zeo Route Planner.

```
POST https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-route" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-route', {
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
| `driverId` | number | yes | Driver id to assign the route. |
| `endAddress` | string | yes | Route end address. |
| `endLatitude` | number | yes | End address latitude. |
| `endLongitude` | number | yes | End address longitude. |
| `original` | boolean | no | Original route generation flag. Default: `true`. |
| `routeDate` | string | no | Route date. |
| `routeName` | string | yes | Name of the route. |
| `startAddress` | string | yes | Route start address. |
| `startLatitude` | number | yes | Start address latitude. |
| `startLongitude` | number | yes | Start address longitude. |
| `stops[]` | array<object> | yes | Stops between route start and end as an array of objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "driverId": 1,
      "endAddress": "string",
      "endLatitude": 1,
      "endLongitude": 1,
      "id": 1,
      "routeDate": "2026-05-07T12:00:00.000Z",
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
| `driverId` | number | Assigned driver identifier. |
| `endAddress` | string | Route end address. |
| `endLatitude` | number | End address latitude. |
| `endLongitude` | number | End address longitude. |
| `id` | number | Route identifier. |
| `routeDate` | date | Route date. |
| `routeName` | string | Route name. |
| `routeStops` | array<object> | Stops included in the route. |
| `startAddress` | string | Route start address. |
| `startLatitude` | number | Start address latitude. |
| `startLongitude` | number | Start address longitude. |

## Native endpoint

Through the native Zeo Route Planner API, this operation is `POST /api/v5/routes` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-route.md) for the provider-specific parameters and requirements.

