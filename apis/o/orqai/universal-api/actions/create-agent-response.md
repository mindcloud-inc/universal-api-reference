# Orq.ai: Create Agent Response

Creates an agent response in Orq.ai.

```
POST https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentKey": "agent_test_key"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentKey": "agent_test_key"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentKey` | string | yes | Agent Key from the Orq.ai path parameter. Example: `agent_test_key`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": "string",
      "output": [
        {
          "messageId": "string",
          "parts": [
            {
              "kind": "string",
              "text": "string"
            }
          ],
          "role": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model` | string |  |
| `output[].messageId` | string |  |
| `output[].parts[].kind` | string |  |
| `output[].parts[].text` | string |  |
| `output[].role` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/agents/[:agent_key]/responses` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-response.md) for the provider-specific parameters and requirements.

