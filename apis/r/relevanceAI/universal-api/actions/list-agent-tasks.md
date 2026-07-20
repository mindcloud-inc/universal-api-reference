# Relevance AI: List Agent Tasks



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agent-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agent-tasks?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agent-tasks?${params}`, {
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
| `agentId` | string | yes |  |
| `pageSize` | number | no | Default: `50`. |
| `search` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "knowledge_set": "string",
      "metadata": {
        "conversation": {
          "agent_id": "string",
          "pending_approvals": [
            {}
          ],
          "state": "string",
          "title": "string"
        },
        "update_datetime": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `knowledge_set` | string | The conversation-backed task ID. |
| `metadata.conversation.agent_id` | string | The agent ID for the task. |
| `metadata.conversation.pending_approvals` | array<object> | Pending approval requests for the task. |
| `metadata.conversation.state` | string | The current task state. |
| `metadata.conversation.title` | string | The task title. |
| `metadata.update_datetime` | date | When the task was last updated. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /agents/conversations/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-tasks.md) for the provider-specific parameters and requirements.

