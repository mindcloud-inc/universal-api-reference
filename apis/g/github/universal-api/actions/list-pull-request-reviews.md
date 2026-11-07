# GitHub: List Pull Request Reviews

Retrieves the reviews submitted on a GitHub pull request.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-pull-request-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-pull-request-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string&pullNumber=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string",
  "pullNumber": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-pull-request-reviews?${params}`, {
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
| `pullNumber` | number | yes | The number that identifies the pull request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": "string",
      "submittedAt": "2026-05-07T12:00:00.000Z",
      "body": "string",
      "htmlUrl": "https://example.com",
      "authorAssociation": "string",
      "commitId": "string",
      "id": 1,
      "nodeId": "string",
      "pullRequestUrl": "https://example.com",
      "isCopilotCodeReview": true,
      "copilotCodeReviewEffort": "string",
      "Links": {
        "html": {
          "href": "https://example.com"
        },
        "pullRequest": {
          "href": "https://example.com"
        }
      },
      "user": {
        "avatarUrl": "https://example.com",
        "eventsUrl": "https://example.com",
        "followersUrl": "https://example.com",
        "followingUrl": "https://example.com",
        "gistsUrl": "https://example.com",
        "gravatarId": "string",
        "htmlUrl": "https://example.com",
        "id": 1,
        "login": "Ava Chen",
        "nodeId": "string",
        "organizationsUrl": "https://example.com",
        "receivedEventsUrl": "https://example.com",
        "reposUrl": "https://example.com",
        "siteAdmin": true,
        "starredUrl": "https://example.com",
        "subscriptionsUrl": "https://example.com",
        "type": "string",
        "url": "https://example.com",
        "userViewType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | string |  |
| `submittedAt` | date |  |
| `body` | string |  |
| `htmlUrl` | string |  |
| `authorAssociation` | string |  |
| `commitId` | string |  |
| `id` | number |  |
| `nodeId` | string |  |
| `pullRequestUrl` | string |  |
| `isCopilotCodeReview` | boolean |  |
| `copilotCodeReviewEffort` | string |  |
| `Links.html.href` | string |  |
| `Links.pullRequest.href` | string |  |
| `user.avatarUrl` | string |  |
| `user.eventsUrl` | string |  |
| `user.followersUrl` | string |  |
| `user.followingUrl` | string |  |
| `user.gistsUrl` | string |  |
| `user.gravatarId` | string |  |
| `user.htmlUrl` | string |  |
| `user.id` | number |  |
| `user.login` | string |  |
| `user.nodeId` | string |  |
| `user.organizationsUrl` | string |  |
| `user.receivedEventsUrl` | string |  |
| `user.reposUrl` | string |  |
| `user.siteAdmin` | boolean |  |
| `user.starredUrl` | string |  |
| `user.subscriptionsUrl` | string |  |
| `user.type` | string |  |
| `user.url` | string |  |
| `user.userViewType` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/pulls/:pull_number/reviews` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pull-request-reviews.md) for the provider-specific parameters and requirements.

