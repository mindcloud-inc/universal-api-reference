# BKK Futar: Get Schedule For Stop

Retrieves the schedule for a selected BKK Futar stop.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-schedule-for-stop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-schedule-for-stop?connectionId=$CONNECTION_ID&stop_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stop_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-schedule-for-stop?${params}`, {
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
| `date` | string | no | Requested date in YYYYMMDD format. |
| `only_departures` | boolean | no | Return departures only. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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
        "date": "string",
        "nearbyStopIds": [
          "string"
        ],
        "routeIds": [
          "string"
        ],
        "schedules": {
          "alertIds": [
            "string"
          ],
          "directions": {
            "directionId": "string",
            "groups": {},
            "stopTimes": [
              {}
            ]
          },
          "routeId": "string"
        },
        "stopId": "string"
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
| `entry.alertIds` | array<string> | Alert IDs related to the stop. |
| `entry.date` | string | Requested schedule date in YYYYMMDD format. |
| `entry.nearbyStopIds` | array<string> | Nearby stop IDs. |
| `entry.routeIds` | array<string> | Route IDs related to the schedule. |
| `entry.schedules` | array<object> | Schedules grouped by route and direction. |
| `entry.schedules.alertIds` | array<string> | Alert IDs for the schedule. |
| `entry.schedules.directions` | array<object> | Schedule data grouped by direction. |
| `entry.schedules.directions.directionId` | string | Direction ID. |
| `entry.schedules.directions.groups` | object | Grouped target stop and schedule details. |
| `entry.schedules.directions.stopTimes` | array<object> | Stop times within the schedule. |
| `entry.schedules.routeId` | string | Relevant route ID. |
| `entry.stopId` | string | Requested stop ID. |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `references` | object | Included reference details. |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /schedule-for-stop.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule-for-stop.md) for the provider-specific parameters and requirements.

