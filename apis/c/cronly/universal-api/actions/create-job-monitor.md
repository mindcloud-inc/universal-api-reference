# Cronly: Create Job Monitor



```
POST https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-job-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-job-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "timezone": "string",
  "schedule": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-job-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "timezone": "string",
    "schedule": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the job monitor. |
| `timezone` | string | yes | Timezone for the monitor schedule. |
| `projectId` | number | no | Optional project to associate with the monitor. |
| `schedule` | string | yes | Cron schedule for the monitor. |
| `duration` | number | yes | Allowed duration in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "schedule": "string",
      "timezone": "string",
      "token": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `created_at` | date |  |
| `duration` | number |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `schedule` | string |  |
| `timezone` | string |  |
| `token` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Cronly API, this operation is `POST /api/monitors` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-monitor.md) for the provider-specific parameters and requirements.

