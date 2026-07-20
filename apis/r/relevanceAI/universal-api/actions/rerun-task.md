# Relevance AI: Rerun Task



```
PUT https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/rerun-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/rerun-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "conversationId": "string",
  "editMessageId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/rerun-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "conversationId": "string",
    "editMessageId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `conversationId` | string | yes |  |
| `editMessageId` | string | yes |  |
| `message` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": "string",
      "conversation_id": "string",
      "job_info": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | string | Agent ID that owns the rerun target. |
| `conversation_id` | string | Conversation ID for the rerun target. |
| `job_info` | object | Job metadata for the rerun request. |
| `state` | string | Immediate provider state after the rerun trigger is submitted. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/trigger` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rerun-task.md) for the provider-specific parameters and requirements.

