# Awork: List User Workloads

Retrieves user workloads from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-user-workloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-user-workloads?connectionId=$CONNECTION_ID&userIds=string&intervalStart=2026-03-20T00%3A00%3A00Z&intervalEnd=2026-03-27T00%3A00%3A00Z&roughPlanningFrom=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIds": "string",
  "intervalStart": "2026-03-20T00:00:00Z",
  "intervalEnd": "2026-03-27T00:00:00Z",
  "roughPlanningFrom": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-user-workloads?${params}`, {
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
| `userIds` | string | yes | Comma-separated awork user IDs to include in the workload response. |
| `intervalStart` | string | yes | UTC timestamp string for the start of the workload interval. Example: `2026-03-20T00:00:00Z`. |
| `intervalEnd` | string | yes | UTC timestamp string for the end of the workload interval. Example: `2026-03-27T00:00:00Z`. |
| `roughPlanningFrom` | number | yes | Number of days from today for including rough planning data. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fetchDetails` | boolean | no | Include contributing project, task, appointment, and absence details. Only works for single-day queries. |
| `ignoreCalendarEvents` | boolean | no | Ignore calendar events when calculating workload. This can improve performance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userId": "string",
      "workloads": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "duration": 1,
          "remainingUserCapacity": 1,
          "userCapacity": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userId` | string |  |
| `workloads[].date` | date |  |
| `workloads[].duration` | number |  |
| `workloads[].remainingUserCapacity` | number |  |
| `workloads[].userCapacity` | number |  |

## Native endpoint

Through the native Awork API, this operation is `GET /users/workload` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-workloads.md) for the provider-specific parameters and requirements.

