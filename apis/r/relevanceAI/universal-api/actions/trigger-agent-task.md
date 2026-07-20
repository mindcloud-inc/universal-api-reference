# Relevance AI: Trigger Agent Task



```
POST https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-agent-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-agent-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-agent-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The Relevance AI agent id to trigger. |
| `role` | string | no | Role for the nested provider message object. Default: `user`. |
| `message` | string | yes | The user message to send to the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": "string",
      "conversation_id": "string",
      "job_info": {
        "job_id": "string",
        "studio_id": "string"
      },
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | string | The triggered agent ID. |
| `conversation_id` | string | The created conversation ID. |
| `job_info.job_id` | string | The job ID. |
| `job_info.studio_id` | string | The internal studio runner ID. |
| `state` | string | The current task state. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/trigger` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-agent-task.md) for the provider-specific parameters and requirements.

