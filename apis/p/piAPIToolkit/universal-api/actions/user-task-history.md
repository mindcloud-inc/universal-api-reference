# PiAPI/Toolkit: User Task History

Retrieves user task history from PiAPI/Toolkit.

```
GET https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/user-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Toolkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/user-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/user-task-history?${params}`, {
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
      "account_id": 1,
      "action": "string",
      "api_key_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "detail": {
        "model": "string",
        "task_id": "string",
        "workflow_type": "string"
      },
      "fixed": true,
      "id": 1,
      "service_mode": "string",
      "status": "string",
      "task_id": "string",
      "task_model": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "usage": 1,
      "usage_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `action` | string |  |
| `api_key_id` | number |  |
| `created_at` | date |  |
| `detail.model` | string |  |
| `detail.task_id` | string |  |
| `detail.workflow_type` | string |  |
| `fixed` | boolean |  |
| `id` | number |  |
| `service_mode` | string |  |
| `status` | string |  |
| `task_id` | string |  |
| `task_model` | string |  |
| `updated_at` | date |  |
| `usage` | number |  |
| `usage_type` | string |  |

## Native endpoint

Through the native PiAPI/Toolkit API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/user-task-history.md) for the provider-specific parameters and requirements.

