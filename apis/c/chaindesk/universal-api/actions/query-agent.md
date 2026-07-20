# Chaindesk: Query Agent

Sends a query to an agent in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/query-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/query-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/query-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `query` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "approvals": [
        "string"
      ],
      "conversationId": "string",
      "messageId": "string",
      "sources": [
        "string"
      ],
      "usage": {
        "completionTokens": 1,
        "cost": 1,
        "promptTokens": 1,
        "totalTokens": 1
      },
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `approvals` | array<string> |  |
| `conversationId` | string |  |
| `messageId` | string |  |
| `sources` | array<string> |  |
| `usage` | object |  |
| `usage.completionTokens` | number |  |
| `usage.cost` | number |  |
| `usage.promptTokens` | number |  |
| `usage.totalTokens` | number |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `POST /agents/:agentId/query` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-agent.md) for the provider-specific parameters and requirements.

