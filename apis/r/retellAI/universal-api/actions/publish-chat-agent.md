# Retell AI: Publish Chat Agent

Publishes a chat agent in Retell AI.

```
PUT https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/publish-chat-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/publish-chat-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/publish-chat-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Retell AI API returns.

## Native endpoint

Through the native Retell AI API, this operation is `POST /publish-chat-agent/{agent_id}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-chat-agent.md) for the provider-specific parameters and requirements.

