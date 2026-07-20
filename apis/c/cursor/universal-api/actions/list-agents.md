# Cursor: List Agents



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-agents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "nextCursor": "string",
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
| `nextCursor` | string | Cursor for the next page of results. |
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

Through the native Cursor API, this operation is `GET /v0/agents` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

