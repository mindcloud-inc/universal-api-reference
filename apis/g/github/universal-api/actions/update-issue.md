# GitHub: Update Issue

Updates an issue in a GitHub repository.

```
PUT https://connect.mindcloud.co/v1/universal/github/latest/actions/update-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/github/latest/actions/update-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "issue_number": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/update-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "issue_number": 1
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
| `issue_number` | number | yes | Issue number. |
| `title` | string | no | The title of the issue. |
| `body` | string | no | The contents of the issue. |
| `state` | list<string> | no | The open or closed state of the issue. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | no | Username to assign to this issue. |
| `state_reason` | list<string> | no | The reason for the state change. One of: `0`, `1`, `2`, `3`. |
| `milestone` | number | no | The milestone number to associate with this issue. |
| `labels[]` | array<string> | no | Labels to associate with this issue. |
| `assignees[]` | array<string> | no | User logins to assign to this issue. |
| `type` | string | no | The issue type name to associate with this issue. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `PATCH /repos/:owner/:repo/issues/:issue_number` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-issue.md) for the provider-specific parameters and requirements.

