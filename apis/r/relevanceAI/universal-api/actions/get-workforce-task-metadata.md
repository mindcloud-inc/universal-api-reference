# Relevance AI: Get Workforce Task Metadata



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce-task-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce-task-metadata?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce-task-metadata?${params}`, {
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
| `taskId` | string | yes | The workforce task id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "chat_mode": "string",
        "insert_date": "2026-05-07T12:00:00.000Z",
        "project": "string",
        "requested_state": "string",
        "state": "string",
        "task_type": "string",
        "title": "string",
        "update_date": "2026-05-07T12:00:00.000Z",
        "workforce_id": "string",
        "workforce_task_id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata.chat_mode` | string | The workforce chat mode. |
| `metadata.insert_date` | date | When the task was created. |
| `metadata.project` | string | The Relevance AI project ID. |
| `metadata.requested_state` | string | The requested state for the task. |
| `metadata.state` | string | The current task state. |
| `metadata.task_type` | string | The workforce task type. |
| `metadata.title` | string | The workforce task title. |
| `metadata.update_date` | date | When the task was last updated. |
| `metadata.workforce_id` | string | The workforce ID. |
| `metadata.workforce_task_id` | string | The workforce task ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /workforce/tasks/:taskId/metadata` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workforce-task-metadata.md) for the provider-specific parameters and requirements.

