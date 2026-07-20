# BKK Futar: Get Arrivals And Departures For Stop

Retrieves arrivals and departures for a BKK Futar stop.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-arrivals-and-departures-for-stop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-arrivals-and-departures-for-stop?connectionId=$CONNECTION_ID&stop_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stop_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-arrivals-and-departures-for-stop?${params}`, {
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
| `only_departures` | boolean | no | Return departures only. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minutes_before` | number | no | Minutes before the query time to include. |
| `minutes_after` | number | no | Minutes after the query time to include. |
| `include_route_id` | string | no | Comma-separated route IDs used to filter results. |
| `time` | number | no | Epoch seconds timestamp used for the query. |
| `limit` | number | no | Maximum number of returned stop times. |
| `lat` | number | no | Latitude information of the location. |
| `lon` | number | no | Longitude information of the location. |
| `radius` | number | no | Radius around latitude and longitude. |
| `query` | string | no | Query expression used to filter results. |
| `min_result` | number | no | Minimum number of elements returned. |
| `include_references` | string | no | Reference data to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {
        "alertIds": [
          "string"
        ],
        "nearbyStopIds": [
          "string"
        ],
        "routeIds": [
          "string"
        ],
        "stopId": "string",
        "stopTimes": {
          "alertIds": [
            "string"
          ],
          "arrivalTime": 1,
          "departureTime": 1,
          "mayRequireBooking": true,
          "predictedArrivalTime": 1,
          "predictedDepartureTime": 1,
          "serviceDate": "string",
          "stopHeadsign": "string",
          "stopId": "string",
          "tripId": "string",
          "uncertain": true,
          "wheelchairAccessible": true
        }
      },
      "limitExceeded": true,
      "references": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry.alertIds` | array<string> | Alert IDs belonging to the stop. |
| `entry.nearbyStopIds` | array<string> | Nearby stop IDs. |
| `entry.routeIds` | array<string> | Route IDs belonging to the stop. |
| `entry.stopId` | string | Requested stop ID. |
| `entry.stopTimes` | array<object> | Arrival and departure stop times. |
| `entry.stopTimes.alertIds` | array<string> | Alert IDs for the stop time. |
| `entry.stopTimes.arrivalTime` | number | Planned arrival time in epoch seconds. |
| `entry.stopTimes.departureTime` | number | Planned departure time in epoch seconds. |
| `entry.stopTimes.mayRequireBooking` | boolean | Whether a later stop may require booking. |
| `entry.stopTimes.predictedArrivalTime` | number | Predicted arrival time in epoch seconds. |
| `entry.stopTimes.predictedDepartureTime` | number | Predicted departure time in epoch seconds. |
| `entry.stopTimes.serviceDate` | string | Service date in YYYYMMDD format. |
| `entry.stopTimes.stopHeadsign` | string | Displayed destination. |
| `entry.stopTimes.stopId` | string | Stop ID for the stop time. |
| `entry.stopTimes.tripId` | string | Trip ID. |
| `entry.stopTimes.uncertain` | boolean | Whether realtime data is uncertain. |
| `entry.stopTimes.wheelchairAccessible` | boolean | Whether the trip is wheelchair accessible. |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `references` | object | Included reference details. |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /arrivals-and-departures-for-stop.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-arrivals-and-departures-for-stop.md) for the provider-specific parameters and requirements.

