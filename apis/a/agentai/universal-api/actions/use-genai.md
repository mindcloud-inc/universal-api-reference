# Agent.ai: Use GenAI

Creates AI-generated text in Agent.ai from instructions.

```
POST https://connect.mindcloud.co/v1/universal/agentai/latest/actions/use-genai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/use-genai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instructions": "string",
  "llmEngine": "gpt4o"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentai/latest/actions/use-genai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instructions": "string",
    "llmEngine": "gpt4o"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instructions` | string | yes | Instructions for the language model. |
| `llmEngine` | string | yes | LLM model to use for text generation. Default: `gpt4o`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Metadata returned with the language-model response, including usage details when present. |
| `response` | string | Generated language-model response text. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/invoke_llm` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/use-genai.md) for the provider-specific parameters and requirements.

