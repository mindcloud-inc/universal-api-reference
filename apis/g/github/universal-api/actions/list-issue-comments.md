# GitHub: List Issue Comments



```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-issue-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-issue-comments?connectionId=$CONNECTION_ID&owner=string&repo=string&issue_number=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "issue_number": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-issue-comments?${params}`, {
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
| `issue_number` | number | yes | The number that identifies the issue or pull request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `per_page` | number | no | The number of results per page (max 100). Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorAssociation": "string",
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "htmlUrl": "https://example.com",
      "id": 1,
      "issueUrl": "https://example.com",
      "nodeId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "avatarUrl": "https://example.com",
        "htmlUrl": "https://example.com",
        "id": 1,
        "login": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorAssociation` | string |  |
| `body` | string |  |
| `createdAt` | date |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `issueUrl` | string |  |
| `nodeId` | string |  |
| `updatedAt` | date |  |
| `user.avatarUrl` | string |  |
| `user.htmlUrl` | string |  |
| `user.id` | number |  |
| `user.login` | string |  |
| `user.type` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/issues/:issue_number/comments` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issue-comments.md) for the provider-specific parameters and requirements.

