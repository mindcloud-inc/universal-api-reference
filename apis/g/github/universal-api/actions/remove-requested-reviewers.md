# GitHub: Remove Requested Reviewers



```
DELETE https://connect.mindcloud.co/v1/universal/github/latest/actions/remove-requested-reviewers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/github/latest/actions/remove-requested-reviewers?connectionId=$CONNECTION_ID&owner=string&repo=string&pull_number=1&reviewers%5B%5D=octocat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "pull_number": "1",
  "reviewers[]": "octocat"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/remove-requested-reviewers?${params}`, {
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
| `pull_number` | number | yes | The number that identifies the pull request. |
| `reviewers[]` | array<string> | yes | User logins that will be removed as requested reviewers. Example: `octocat`. |
| `team_reviewers[]` | array<string> | no | Team slugs that will be removed as requested reviewers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "draft": true,
      "htmlUrl": "https://example.com",
      "id": 1,
      "nodeId": "string",
      "number": 1,
      "requestedReviewers": [
        {
          "login": "Ava Chen"
        }
      ],
      "requestedTeams": [
        {
          "slug": "string"
        }
      ],
      "state": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "login": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `draft` | boolean |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `nodeId` | string |  |
| `number` | number |  |
| `requestedReviewers[].login` | string |  |
| `requestedTeams[].slug` | string |  |
| `state` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `user.login` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `DELETE /repos/:owner/:repo/pulls/:pull_number/requested_reviewers` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-requested-reviewers.md) for the provider-specific parameters and requirements.

