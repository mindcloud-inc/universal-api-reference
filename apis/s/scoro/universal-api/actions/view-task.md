# Scoro: View Task

Retrieves task details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-task?${params}`, {
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
| `id` | string | no | Scoro task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity_id": 1,
      "activity_type": "string",
      "assigned_to": 1,
      "datetime_due": "string",
      "duration_actual": "string",
      "duration_planned": "string",
      "event_id": 1,
      "event_name": "Ava Chen",
      "is_completed": 1,
      "project_id": 1,
      "project_name": "Ava Chen",
      "start_datetime": "string",
      "status": "string",
      "status_name": "Ava Chen",
      "time_entries": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity_id` | number |  |
| `activity_type` | string |  |
| `assigned_to` | number |  |
| `datetime_due` | string |  |
| `duration_actual` | string |  |
| `duration_planned` | string |  |
| `event_id` | number |  |
| `event_name` | string |  |
| `is_completed` | number |  |
| `project_id` | number |  |
| `project_name` | string |  |
| `start_datetime` | string |  |
| `status` | string |  |
| `status_name` | string |  |
| `time_entries` | array<object> |  |

## Native endpoint

Through the native Scoro API, this operation is `POST tasks/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-task.md) for the provider-specific parameters and requirements.

