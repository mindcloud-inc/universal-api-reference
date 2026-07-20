# Chatvolt AI: Agent Query

Sends a query to an agent in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the agent to be queried. |
| `query` | string | yes | Text of the question or command to be sent to the agent. |
| `streaming` | boolean | no | Set to `true` to receive a Server-Sent Events (SSE) stream, `false` for a single JSON response. |
| `conversationId` | string | no | ID of the existing conversation. If not provided or invalid, a new conversation will be created. |
| `contactId` | string | no | ID of an existing contact in the system. If provided, associates the conversation with this contact. Alternative to the `contact` object. |
| `contact` | object | no | Contact details. Used to find an existing contact (by email, phoneNumber, or userId) or create a new one if not found. |
| `visitorId` | string | no | ID of the visitor/participant who is sending the query. If not provided, a new ID will be generated. |
| `temperature` | number | no | Model temperature (min 0.0, max 1.0). Controls the randomness of the response. |
| `modelName` | string | no | Allows overriding the LLM model configured in the agent for this specific query. Use [valid model names](https://api.chatvolt.ai/agents/models). |
| `presencePenalty` | number | no | Presence penalty (between -2.0 and 2.0). Positive values encourage the model to talk about new topics. |
| `frequencyPenalty` | number | no | Frequency penalty (between -2.0 and 2.0). Positive values discourage the model from repeating textual lines. |
| `topP` | number | no | Nucleus sampling (alternative to temperature). Considers tokens with accumulated probability mass top_p. (Ex: 0.1 considers the top 10%). It is recommended to change `topP` or `temperature`, not both. |
| `filters` | object | no | Filters for application/json requests. |
| `systemPrompt` | string | no | Allows overriding the system prompt configured in the agent for this specific query. |
| `context` | object | no | Object to pass additional context data that can be used by tools or in the prompt. |
| `callbackURL` | string | no | Optional URL. If provided, the API will return 202 immediately and will deliver the response to the Agent via a POST request to this URL when it is ready. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "conversationId": "string",
      "messageId": "string",
      "metadata": {},
      "sources": [
        "string"
      ],
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | The agent's textual response. |
| `conversationId` | string | ID of the conversation (existing or new). |
| `messageId` | string | ID of the agent's response message in the database. |
| `metadata` | object | Additional metadata returned (may vary). |
| `sources` | array | Datasource chunks used to generate the response (if applicable). |
| `visitorId` | string | ID of the visitor/participant. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /agents/{id}/query` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-query.md) for the provider-specific parameters and requirements.

