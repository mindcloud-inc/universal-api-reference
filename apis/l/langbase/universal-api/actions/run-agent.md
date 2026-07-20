# Langbase: Run Agent



```
POST https://connect.mindcloud.co/v1/universal/langbase/latest/actions/run-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/run-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/run-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | LLM model to run the agent with. |
| `input` | string | yes | Prompt or user input for the agent run. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `llmApiKey` | string | no | Provider LLM API key for the `LB-LLM-Key` request header when the selected model is not already configured in Langbase. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `POST v1/agent/run` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-agent.md) for the provider-specific parameters and requirements.

