# Relevance AI: View Task Steps



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/view-agent-task-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/view-agent-task-steps?connectionId=$CONNECTION_ID&agentId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/view-agent-task-steps?${params}`, {
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
| `agentId` | string | yes | The Relevance AI agent id. |
| `conversationId` | string | yes | The task or conversation id to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {
        "agent_details": {
          "name": "Ava Chen"
        },
        "text": "string",
        "trigger_source": "string",
        "type": "string"
      },
      "insert_date_": "2026-05-07T12:00:00.000Z",
      "item_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content.agent_details.name` | string | The agent display name. |
| `content.text` | string | The item text. |
| `content.trigger_source` | string | The trigger source for trigger messages. |
| `content.type` | string | The item content type. |
| `insert_date_` | date | When the item was created. |
| `item_id` | string | The task item ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/:agentId/tasks/:conversationId/view` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-agent-task-steps.md) for the provider-specific parameters and requirements.

