# Devin: Get Schedule

Retrieves a schedule record from Devin.

```
GET https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-schedule?connectionId=$CONNECTION_ID&orgId=string&scheduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "scheduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-schedule?${params}`, {
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
| `orgId` | string | yes | Devin organization ID. |
| `scheduleId` | string | yes | Scheduled session ID. |

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

Through the native Devin API, this operation is `GET /v3/organizations/:org_id/schedules/:schedule_id` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

