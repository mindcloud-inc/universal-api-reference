# NeroBot AI: Query AI Task Result

Retrieves an AI task result from NeroBot AI.

```
GET https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/query-ai-task-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeroBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/query-ai-task-result?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/query-ai-task-result?${params}`, {
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
| `taskId` | string | yes | Task ID returned by Create AI Task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "output": "string"
      },
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.output` | string |  |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native NeroBot AI API, this operation is `GET /biz/api/task` (base URL `https://api.nero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-ai-task-result.md) for the provider-specific parameters and requirements.

