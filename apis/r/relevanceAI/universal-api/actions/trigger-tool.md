# Relevance AI: Trigger Tool



```
POST https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "toolId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "toolId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | The Relevance AI project ID. Use the same project value as your connection. |
| `toolId` | string | yes | The Relevance AI tool id to run. |
| `params` | object | no | Optional params object to pass into the tool run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "output": {
        "executionTime": 1,
        "status": "string",
        "transformed": {
          "first_number": 1,
          "result": 1,
          "second_number": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `output.executionTime` | number | The tool execution time. |
| `output.status` | string | The tool run status. |
| `output.transformed.first_number` | number | The first number passed to the tool. |
| `output.transformed.result` | number | The tool result. |
| `output.transformed.second_number` | number | The second number passed to the tool. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /studios/:toolId/trigger_limited` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-tool.md) for the provider-specific parameters and requirements.

