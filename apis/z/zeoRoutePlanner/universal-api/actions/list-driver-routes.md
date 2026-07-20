# Zeo Route Planner: List Driver Routes

Retrieves routes for a driver in Zeo Route Planner.

```
GET https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-driver-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-driver-routes?connectionId=$CONNECTION_ID&driverId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driverId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-driver-routes?${params}`, {
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
| `driverId` | number | yes | Driver id whose routes to list. |
| `limit` | number | no | Records to return. Default: `50`. |
| `offset` | number | no | Next records to return. Default: `0`. |

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

Through the native Zeo Route Planner API, this operation is `GET /api/v5/routes` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-driver-routes.md) for the provider-specific parameters and requirements.

