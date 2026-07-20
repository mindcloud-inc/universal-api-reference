# Mona AI: Get Agent Response

Gets a response from a Mona AI agent.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agent-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agent-response?connectionId=$CONNECTION_ID&agentId=string&permission=string&prompt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "permission": "string",
  "prompt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agent-response?${params}`, {
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
| `additional_info` | string | no | Optional additional context for the agent request. |
| `agentId` | string | yes | Mona agent identifier to execute. |
| `document_link` | string | no | Optional document link to include with the agent request. |
| `document_name` | string | no | Optional document name to include with the agent request. |
| `language_code` | string | no | Language code for the agent response; docs default to DE. |
| `permission` | string | yes | Mona permission string for agent execution; docs show executeAgents for this endpoint. |
| `prompt` | string | yes | Prompt to send to the agent. |
| `session_id` | string | no | Agent session identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /agent/getAgentResponse` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-response.md) for the provider-specific parameters and requirements.

