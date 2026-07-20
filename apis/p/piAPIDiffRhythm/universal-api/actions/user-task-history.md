# PiAPI/DiffRhythm: User Task History

Retrieves your task history from PiAPI/DiffRhythm.

```
GET https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/user-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/DiffRhythm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/user-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/user-task-history?${params}`, {
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
| `page` | number | no | History page number starting at 1. Default: `1`. |
| `pageSize` | number | no | Number of history records to return. PiAPI allows up to 100. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startTime` | number | no | Optional Unix timestamp in seconds. Only return tasks created after this time. |
| `endTime` | number | no | Optional Unix timestamp in seconds. Only return tasks created before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "page": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].account_id` | number |  |
| `data[].action` | string |  |
| `data[].api_key_id` | number |  |
| `data[].created_at` | date |  |
| `data[].detail.model` | string |  |
| `data[].detail.task_id` | string |  |
| `data[].detail.workflow_type` | string |  |
| `data[].fixed` | boolean |  |
| `data[].id` | number |  |
| `data[].service_mode` | string |  |
| `data[].status` | string |  |
| `data[].task_id` | string |  |
| `data[].task_model` | string |  |
| `data[].updated_at` | date |  |
| `data[].usage` | number |  |
| `data[].usage_type` | string |  |
| `page` | number |  |
| `size` | number |  |
| `total` | number |  |

## Native endpoint

Through the native PiAPI/DiffRhythm API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/user-task-history.md) for the provider-specific parameters and requirements.

