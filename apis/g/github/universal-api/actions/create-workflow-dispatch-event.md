# GitHub: Create Workflow Dispatch Event

Triggers a GitHub Actions workflow run.

```
POST https://connect.mindcloud.co/v1/universal/github/latest/actions/create-workflow-dispatch-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/github/latest/actions/create-workflow-dispatch-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "workflow_id": "string",
  "ref": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/create-workflow-dispatch-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "workflow_id": "string",
    "ref": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `workflow_id` | string | yes | The workflow ID or workflow file name. |
| `ref` | string | yes | The git reference for the workflow. The reference can be a branch or tag name. |
| `inputs` | object | no | Input keys and values configured in the workflow file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `return_run_details` | boolean | no | Whether the response should include the workflow run ID and URLs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `POST /repos/:owner/:repo/actions/workflows/:workflow_id/dispatches` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow-dispatch-event.md) for the provider-specific parameters and requirements.

