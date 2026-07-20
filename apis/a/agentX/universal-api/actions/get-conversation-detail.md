# AgentX: Get Conversation Detail

Retrieves conversation details from AgentX.

```
GET https://connect.mindcloud.co/v1/universal/agentX/latest/actions/get-conversation-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AgentX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentX/latest/actions/get-conversation-detail?connectionId=$CONNECTION_ID&agentId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentX/latest/actions/get-conversation-detail?${params}`, {
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
| `agentId` | string | yes | Agent Id |
| `conversationId` | string | yes | Conversation Id |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AgentX API returns.

## Native endpoint

Through the native AgentX API, this operation is `GET /agents/:id/conversations/:cid` (base URL `https://api.agentx.so/api/v1/access`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-detail.md) for the provider-specific parameters and requirements.

