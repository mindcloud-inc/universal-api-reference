# BKK Futar: Get Vehicles For Stop

Retrieves vehicles on routes containing a selected BKK Futar stop.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-vehicles-for-stop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-vehicles-for-stop?connectionId=$CONNECTION_ID&stop_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stop_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-vehicles-for-stop?${params}`, {
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
| `stop_id` | string | yes | Stop ID to query, such as BKK_F01227. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `if_modified_since` | number | no | Return data modified since this UNIX timestamp. |
| `include_references` | string | no | Reference data to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limitExceeded": true,
      "list": {
        "bearing": 1,
        "capacity": {},
        "deviated": true,
        "label": "string",
        "lastUpdateTime": 1,
        "licensePlate": "string",
        "location": {
          "lat": 1,
          "lon": 1
        },
        "occupancy": {},
        "routeId": "string",
        "status": "string",
        "stopDistancePercent": 1,
        "stopId": "string",
        "stopSequence": 1,
        "tripId": "string",
        "vehicleId": "string",
        "vertex": "string",
        "wheelchairAccessible": true
      },
      "references": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `list` | array<object> | Vehicles on routes containing the selected stop. |
| `list.bearing` | number | Vehicle bearing. |
| `list.capacity` | object | Vehicle capacity details. |
| `list.deviated` | boolean | Whether the vehicle has deviated from route. |
| `list.label` | string | Vehicle label. |
| `list.lastUpdateTime` | number | Last realtime update timestamp. |
| `list.licensePlate` | string | License plate. |
| `list.location` | object | Vehicle location. |
| `list.location.lat` | number | Vehicle latitude. |
| `list.location.lon` | number | Vehicle longitude. |
| `list.occupancy` | object | Vehicle occupancy details. |
| `list.routeId` | string | Route ID. |
| `list.status` | string | Vehicle status. |
| `list.stopDistancePercent` | number | Percent between stops. |
| `list.stopId` | string | Stop ID. |
| `list.stopSequence` | number | Stop sequence for the vehicle. |
| `list.tripId` | string | Trip ID. |
| `list.vehicleId` | string | Vehicle ID. |
| `list.vertex` | string | Journey planner trip identifier. |
| `list.wheelchairAccessible` | boolean | Whether the vehicle is wheelchair accessible. |
| `references` | object | Included reference details. |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /vehicles-for-stop.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vehicles-for-stop.md) for the provider-specific parameters and requirements.

