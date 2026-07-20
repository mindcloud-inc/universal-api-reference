# Cursor: Get Agent Status



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-status?connectionId=$CONNECTION_ID&id=bc_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bc_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-status?${params}`, {
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
| `id` | string | yes | Unique identifier for the cloud agent, for example `bc_abc123`. Example: `bc_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "source": {
        "ref": "string",
        "repository": "string"
      },
      "status": "string",
      "summary": "string",
      "target": {
        "autoCreatePr": true,
        "branchName": "Ava Chen",
        "openAsCursorGithubApp": true,
        "prUrl": "https://example.com",
        "skipReviewerRequest": true,
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the agent was created. |
| `id` | string | Unique cloud agent identifier. |
| `name` | string | Agent name. |
| `source.ref` | string | Git ref used as the base branch. |
| `source.repository` | string | GitHub repository URL. |
| `status` | string | Current cloud agent status. |
| `summary` | string | Summary of the agent work, when available. |
| `target.autoCreatePr` | boolean | Whether Cursor will automatically create a pull request. |
| `target.branchName` | string | Git branch where the agent is working. |
| `target.openAsCursorGithubApp` | boolean | Whether the PR is opened by the Cursor GitHub App. |
| `target.prUrl` | string | Pull request URL, if any. |
| `target.skipReviewerRequest` | boolean | Whether reviewer request is skipped. |
| `target.url` | string | Cursor Web URL for the agent. |

## Native endpoint

Through the native Cursor API, this operation is `GET /v0/agents/{{id}}` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-status.md) for the provider-specific parameters and requirements.

