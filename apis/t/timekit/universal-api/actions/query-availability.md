# Timekit: Query Availability

Finds available booking timeslots in Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/query-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/query-availability?connectionId=$CONNECTION_ID&mode=exclusive" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mode": "exclusive"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/query-availability?${params}`, {
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
| `buffer` | string | no | Buffer time around existing events. |
| `constraints[]` | array<object> | no | Availability constraint objects. |
| `from` | string | no | Beginning of the search space. |
| `length` | string | no | Length of each available time slot. |
| `mode` | list<string> | yes | Availability mode. One of: `exclusive`, `mutual`, `roundrobin_prioritized`, `roundrobin_random`. |
| `outputTimezone` | string | no | Timezone for returned time slots. |
| `projectId` | string | no | Project ID to derive availability settings from. |
| `resources[]` | array<string> | no | Resource IDs to include in the availability search. |
| `roundToNearestHour` | boolean | no | Round timeslots to the nearest hour. |
| `timeslotIncrements` | string | no | Increments used for time slot starts. |
| `to` | string | no | End of the search space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "resources": [
        {
          "id": "string",
          "name": "Ava Chen",
          "timezone": "string"
        }
      ],
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `resources` | array<object> |  |
| `resources[].id` | string |  |
| `resources[].name` | string |  |
| `resources[].timezone` | string |  |
| `start` | date |  |

## Native endpoint

Through the native Timekit API, this operation is `POST /availability` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-availability.md) for the provider-specific parameters and requirements.

