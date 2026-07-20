# PromptLayer Run Agent: Get Agent Execution Results

Retrieves execution results for a PromptLayer workflow.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-agent-execution-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-agent-execution-results?connectionId=$CONNECTION_ID&workflowVersionExecutionId=13158708" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowVersionExecutionId": "13158708"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-agent-execution-results?${params}`, {
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
| `workflowVersionExecutionId` | number | yes | The PromptLayer workflow execution ID returned by `Run Agent`. Example: `13158708`. |
| `returnAllOutputs` | boolean | no | Whether to return all output nodes instead of only the main output. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PromptLayer Run Agent API returns.

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /workflow-version-execution-results` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-execution-results.md) for the provider-specific parameters and requirements.

