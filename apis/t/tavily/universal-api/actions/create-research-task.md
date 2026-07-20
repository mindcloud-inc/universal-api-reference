# Tavily: Create Research Task

Creates a research task in Tavily.

```
POST https://connect.mindcloud.co/v1/universal/tavily/latest/actions/create-research-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tavily `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/create-research-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tavily/latest/actions/create-research-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `citationFormat` | string | no | Citation format. Accepted values are numbered, mla, apa, or chicago. |
| `input` | string | yes | The research task or question to investigate. |
| `model` | string | no | Research model. Accepted values are mini, pro, or auto. |
| `outputSchema` | object | no | Optional JSON Schema object that defines the research output shape. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "input": "string",
      "model": "string",
      "request_id": "string",
      "response_time": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Timestamp when the research task was created. |
| `input` | string | The research task or question being investigated. |
| `model` | string | The research model used by Tavily. |
| `request_id` | string | Unique request identifier for the research task. |
| `response_time` | number | Time in seconds it took to complete the request. |
| `status` | string | Current status of the research task. |

## Native endpoint

Through the native Tavily API, this operation is `POST /research` (base URL `https://api.tavily.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-research-task.md) for the provider-specific parameters and requirements.

