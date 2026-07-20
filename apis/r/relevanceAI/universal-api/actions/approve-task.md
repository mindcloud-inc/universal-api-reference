# Relevance AI: Approve Task



```
PUT https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/approve-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/approve-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "actionRequestId": "string",
  "agentId": "string",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/approve-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "actionRequestId": "string",
    "agentId": "string",
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes |  |
| `actionRequestId` | string | yes |  |
| `agentId` | string | yes |  |
| `conversationId` | string | yes |  |

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
| `agent_id` | string | Agent ID that owns the approved task. |
| `conversation_id` | string | Conversation ID for the approved task. |
| `job_info` | object | Job metadata for the approved continuation request. |
| `state` | string | Immediate provider state after the approval trigger is submitted. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/trigger` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-task.md) for the provider-specific parameters and requirements.

