# Relevance AI: List Workforce Tasks



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-workforce-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-workforce-tasks?connectionId=$CONNECTION_ID&workforceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workforceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-workforce-tasks?${params}`, {
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
| `workforceId` | string | yes | The workforce id to list tasks for. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_mode` | string | The workforce chat mode. |
| `insert_date` | date | When the task was created. |
| `project` | string | The Relevance AI project ID. |
| `requested_state` | string | The requested state for the task. |
| `state` | string | The current task state. |
| `task_type` | string | The workforce task type. |
| `title` | string | The workforce task title. |
| `update_date` | date | When the task was last updated. |
| `workforce_id` | string | The workforce ID. |
| `workforce_task_id` | string | The workforce task ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /workforce/tasks/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workforce-tasks.md) for the provider-specific parameters and requirements.

