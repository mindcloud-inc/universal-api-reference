# Mona AI: Get Monari Agent Response

Gets a response from a Mona AI Monari agent.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-monari-agent-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-monari-agent-response?connectionId=$CONNECTION_ID&agentId=string&permission=string&prompt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "permission": "string",
  "prompt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-monari-agent-response?${params}`, {
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
| `agentId` | string | yes | Monari agent identifier to execute. |
| `language_code` | string | no | Language code for the response; docs default to DE. |
| `permission` | string | yes | Mona permission string required by the Monari agent response endpoint. |
| `prompt` | string | yes | Prompt to send to the Monari agent. |
| `sessionId` | string | no | Monari agent session identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /agent/getMonariAgentResponse` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monari-agent-response.md) for the provider-specific parameters and requirements.

