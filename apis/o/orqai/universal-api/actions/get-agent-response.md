# Orq.ai: Get Agent Response

Retrieves an agent response from Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/get-agent-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/get-agent-response?connectionId=$CONNECTION_ID&agentKey=agent_test_key&taskId=task_test_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentKey": "agent_test_key",
  "taskId": "task_test_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/get-agent-response?${params}`, {
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
| `agentKey` | string | yes | Agent Key from the Orq.ai path parameter. Example: `agent_test_key`. |
| `taskId` | string | yes | Task ID from the Orq.ai path parameter. Example: `task_test_id`. |

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
          "metadata": {
            "choice": {
              "index": 1,
              "message": {
                "content": "string",
                "role": "string"
              }
            }
          },
          "parts": [
            {
              "kind": "string",
              "text": "string"
            }
          ],
          "role": "string"
        }
      ],
      "status": "string"
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
| `output[].metadata.choice.index` | number |  |
| `output[].metadata.choice.message.content` | string |  |
| `output[].metadata.choice.message.role` | string |  |
| `output[].parts[].kind` | string |  |
| `output[].parts[].text` | string |  |
| `output[].role` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `GET /v2/agents/[:agent_key]/responses/[:task_id]` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-response.md) for the provider-specific parameters and requirements.

