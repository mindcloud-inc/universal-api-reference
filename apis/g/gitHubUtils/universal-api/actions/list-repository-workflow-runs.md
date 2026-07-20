# GitHub Utils: List Repository Workflow Runs

Retrieves workflow runs from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-repository-workflow-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-repository-workflow-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-repository-workflow-runs?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "total_count": 1,
      "workflow_runs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total_count` | number |  |
| `workflow_runs` | array<object> |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/actions/runs` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-repository-workflow-runs.md) for the provider-specific parameters and requirements.

