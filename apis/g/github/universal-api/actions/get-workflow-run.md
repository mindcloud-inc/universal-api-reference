# GitHub: Get Workflow Run

Retrieves a workflow run from GitHub.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/get-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/get-workflow-run?connectionId=$CONNECTION_ID&owner=string&repo=string&run_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "run_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/get-workflow-run?${params}`, {
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
| `owner` | string | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | string | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `run_id` | number | yes | The unique identifier of the workflow run. |
| `exclude_pull_requests` | boolean | no | If true, omit pull requests from the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/actions/runs/:run_id` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-run.md) for the provider-specific parameters and requirements.

