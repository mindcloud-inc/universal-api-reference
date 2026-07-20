# Mona AI: Get Agent Workflow

Retrieves a workflow for a Mona AI agent.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agent-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agent-workflow?connectionId=$CONNECTION_ID&agentId=string&permission=string&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "permission": "string",
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agent-workflow?${params}`, {
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
| `agentId` | string | yes | Mona agent identifier that owns the workflow. |
| `permission` | string | yes | Mona permission string required by this workflow lookup endpoint. |
| `workflowId` | string | yes | Mona workflow identifier to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /agent/getAgentWorkflow` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-workflow.md) for the provider-specific parameters and requirements.

