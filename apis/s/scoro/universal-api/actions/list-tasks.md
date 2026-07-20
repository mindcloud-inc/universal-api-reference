# Scoro: List Tasks

Retrieves tasks from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "event_id": 1,
      "event_name": "Ava Chen",
      "is_completed": 1,
      "project_id": 1,
      "start_datetime": "string",
      "status": "string"
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
| `event_id` | number |  |
| `event_name` | string |  |
| `is_completed` | number |  |
| `project_id` | number |  |
| `start_datetime` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST tasks/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

