# Agent700: Get Workflow by ID



```
GET https://connect.mindcloud.co/v1/universal/agent700/latest/actions/get-workflow-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent700 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agent700/latest/actions/get-workflow-by-id?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agent700/latest/actions/get-workflow-by-id?${params}`, {
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
| `workflowId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agent700 API returns.

## Native endpoint

Through the native Agent700 API, this operation is `GET /workflows/:workflow_id` (base URL `https://api.agent700.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-by-id.md) for the provider-specific parameters and requirements.

