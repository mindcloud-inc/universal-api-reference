# Relevance AI: Schedule Action In Task



```
POST https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/schedule-agent-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/schedule-agent-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "conversationId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/schedule-agent-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "conversationId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The Relevance AI agent id. |
| `conversationId` | string | yes | The task conversation id to schedule against. |
| `message` | string | yes | The follow-up message to schedule. |
| `minutesUntilSchedule` | number | no | How many minutes from now to schedule the action. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trigger_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trigger_id` | string | The scheduled trigger ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/:agentId/scheduled_triggers_item/create` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-agent-action.md) for the provider-specific parameters and requirements.

