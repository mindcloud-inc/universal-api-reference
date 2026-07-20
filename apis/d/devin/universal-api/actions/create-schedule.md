# Devin: Create Schedule

Creates a new schedule in Devin.

```
POST https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "orgId": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "orgId": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agent` | string | no | Agent type: devin, data_analyst, or advanced. |
| `bypassApproval` | boolean | no | Whether to bypass approval for scheduled sessions. |
| `frequency` | string | no | Cron expression for recurring schedules. |
| `name` | string | yes | Schedule name. |
| `notifyOn` | string | no | Notification policy: always, failure, or never. |
| `orgId` | string | yes | Devin organization ID. |
| `prompt` | string | yes | Prompt to run for scheduled sessions. |
| `scheduledAt` | date | no | ISO 8601 datetime for one-time schedules. |
| `scheduleType` | string | no | Schedule type: recurring or one_time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": "string",
      "bypass_approval": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "enabled": true,
      "frequency": "string",
      "interval_count": 1,
      "last_edited_by": "string",
      "last_executed_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notify_on": "string",
      "org_id": "string",
      "prompt": "string",
      "schedule_type": "string",
      "scheduled_at": "2026-05-07T12:00:00.000Z",
      "scheduled_session_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | string | Agent type. |
| `bypass_approval` | boolean | Whether approval is bypassed. |
| `created_at` | date | Creation time. |
| `created_by` | string | Creator identifier. |
| `enabled` | boolean | Whether the schedule is enabled. |
| `frequency` | string | Cron frequency for recurring schedules. |
| `interval_count` | number | Interval count. |
| `last_edited_by` | string | Last editor identifier. |
| `last_executed_at` | date | Last execution time. |
| `name` | string | Schedule name. |
| `notify_on` | string | Notification policy. |
| `org_id` | string | Organization ID. |
| `prompt` | string | Schedule prompt. |
| `schedule_type` | string | Schedule type. |
| `scheduled_at` | date | One-time scheduled execution time. |
| `scheduled_session_id` | string | Scheduled session ID. |
| `updated_at` | date | Update time. |

## Native endpoint

Through the native Devin API, this operation is `POST /v3/organizations/:org_id/schedules` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

