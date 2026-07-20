# Court Drive: Get Async Request Progress



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-async-request-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-async-request-progress?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-async-request-progress?${params}`, {
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
| `taskId` | string | yes | Async task identifier returned by CourtAPI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "completed_tasks": 1,
      "created": "string",
      "error": 1,
      "pending": 1,
      "progress_percent": 1,
      "success": 1,
      "task_id": "string",
      "task_progress": 1,
      "tasks": 1,
      "total": 1,
      "unsent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `completed_tasks` | number |  |
| `created` | string |  |
| `error` | number |  |
| `pending` | number |  |
| `progress_percent` | number |  |
| `success` | number |  |
| `task_id` | string |  |
| `task_progress` | number |  |
| `tasks` | number |  |
| `total` | number |  |
| `unsent` | number |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /progress/{task_id}` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-request-progress.md) for the provider-specific parameters and requirements.

