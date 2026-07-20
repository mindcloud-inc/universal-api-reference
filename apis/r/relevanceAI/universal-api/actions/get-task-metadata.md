# Relevance AI: Get Task Metadata



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-task-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-task-metadata?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-task-metadata?${params}`, {
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
| `conversationId` | string | yes | The task conversation id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "conversation": {
          "agent_id": "string",
          "pending_approvals": [
            {}
          ],
          "state": "string",
          "title": "string"
        },
        "knowledge_set": "string",
        "project": "string",
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
| `metadata.conversation.agent_id` | string | The agent ID. |
| `metadata.conversation.pending_approvals` | array<object> | Pending approval entries for the task. |
| `metadata.conversation.state` | string | The task state. |
| `metadata.conversation.title` | string | The task title. |
| `metadata.knowledge_set` | string | The conversation-backed task ID. |
| `metadata.project` | string | The Relevance AI project ID. |
| `metadata.update_datetime` | date | When the task was last updated. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /knowledge/sets/:conversationId/get_metadata` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-metadata.md) for the provider-specific parameters and requirements.

