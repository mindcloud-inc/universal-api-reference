# Relevance AI: Get Workforce Task Messages



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce-task-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce-task-messages?connectionId=$CONNECTION_ID&workforceId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workforceId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce-task-messages?${params}`, {
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
| `workforceId` | string | yes | The workforce id. |
| `taskId` | string | yes | The workforce task id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {
        "agent_details": {
          "emoji": "string",
          "name": "Ava Chen"
        },
        "node_id": "string",
        "task_details": {
          "conversation_id": "string",
          "current_state": "string",
          "finished_state": "string"
        },
        "text": "string",
        "type": "string"
      },
      "insert_date_": "2026-05-07T12:00:00.000Z",
      "is_expanded_by_default": true,
      "is_in_hidden_group": true,
      "item_id": "string",
      "parent_item_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content.agent_details.emoji` | string | The agent icon or emoji. |
| `content.agent_details.name` | string | The agent name when the item comes from an agent. |
| `content.node_id` | string | The originating workforce node ID. |
| `content.task_details.conversation_id` | string | The related conversation ID when present. |
| `content.task_details.current_state` | string | The related conversation current state when present. |
| `content.task_details.finished_state` | string | The related conversation finished state when present. |
| `content.text` | string | The message text when present. |
| `content.type` | string | The message content type. |
| `insert_date_` | date | When the message item was created. |
| `is_expanded_by_default` | boolean | Whether the item is expanded by default. |
| `is_in_hidden_group` | boolean | Whether the item is in a hidden group. |
| `item_id` | string | The workforce message item ID. |
| `parent_item_id` | string | The parent item ID when present. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /workforce/items/:workforceId/tasks/:taskId/messages` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workforce-task-messages.md) for the provider-specific parameters and requirements.

