# Strategypoint: Get Schedule

Retrieves a schedule from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-schedule?connectionId=$CONNECTION_ID&scheduleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-schedule?${params}`, {
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
| `scheduleId` | number | yes | The unique schedule identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "enabled": true,
      "lastRun": "string",
      "name": "Ava Chen",
      "nextRun": "string",
      "recurrence": "string",
      "scheduleId": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the schedule is active. |
| `enabled` | boolean | Whether the schedule is enabled. |
| `lastRun` | string | The last run timestamp. |
| `name` | string | The schedule name. |
| `nextRun` | string | The next scheduled run timestamp. |
| `recurrence` | string | The recurrence rule for the schedule. |
| `scheduleId` | number | The unique schedule identifier. |
| `state` | string | The current schedule state. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /schedules/{scheduleId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

