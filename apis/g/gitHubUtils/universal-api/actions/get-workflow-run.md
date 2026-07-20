# GitHub Utils: Get Workflow Run

Retrieves a workflow run from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-workflow-run?connectionId=$CONNECTION_ID&owner=string&repo=string&run_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "run_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-workflow-run?${params}`, {
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
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `run_id` | number | yes | GitHub Actions workflow run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actor": {},
      "artifacts_url": "https://example.com",
      "conclusion": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_title": "string",
      "event": "string",
      "head_branch": "string",
      "head_commit": {},
      "head_sha": "string",
      "html_url": "https://example.com",
      "id": 1,
      "jobs_url": "https://example.com",
      "logs_url": "https://example.com",
      "name": "Ava Chen",
      "node_id": "string",
      "path": "string",
      "pull_requests": [
        {}
      ],
      "repository": {},
      "run_attempt": 1,
      "run_number": 1,
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "workflow_id": 1,
      "workflow_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor` | object |  |
| `artifacts_url` | string |  |
| `conclusion` | string |  |
| `created_at` | date |  |
| `display_title` | string |  |
| `event` | string |  |
| `head_branch` | string |  |
| `head_commit` | object |  |
| `head_sha` | string |  |
| `html_url` | string |  |
| `id` | number |  |
| `jobs_url` | string |  |
| `logs_url` | string |  |
| `name` | string |  |
| `node_id` | string |  |
| `path` | string |  |
| `pull_requests` | array<object> |  |
| `repository` | object |  |
| `run_attempt` | number |  |
| `run_number` | number |  |
| `status` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `workflow_id` | number |  |
| `workflow_url` | string |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/actions/runs/:run_id` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-run.md) for the provider-specific parameters and requirements.

