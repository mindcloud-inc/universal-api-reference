# SVAHNAR: Test Agent

Tests an agent in SVAHNAR.

```
POST https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/test-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/test-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "yamlString": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/test-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "yamlString": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | The message or command to send to the test agent. |
| `yamlString` | string | yes | YAML string to test the agent. |
| `threadId` | string | no | Optional unique identifier for the chat session. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentHistory` | string | no | Optional prior messages as a string payload. |
| `hitlDecision` | list | no | Optional human-in-the-loop decision. One of: `approve`, `edit`, `reject`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additional_metadata": {},
      "request_metadata": {},
      "response": [
        {}
      ],
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional_metadata` | object | Additional metadata such as the thread ID. |
| `request_metadata` | object | Response metadata including the request ID. |
| `response` | array<object> | Conversation response blocks returned by the agent test. |
| `usage` | object | Credit usage summary for the test run. |

## Native endpoint

Through the native SVAHNAR API, this operation is `POST /v1/agents/test` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-agent.md) for the provider-specific parameters and requirements.

