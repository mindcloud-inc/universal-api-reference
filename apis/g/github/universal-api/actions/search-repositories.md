# GitHub: Search Repositories

Finds repositories in GitHub by search query.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/search-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/search-repositories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/search-repositories?${params}`, {
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
| `q` | string | no | Optional free-text search terms or prebuilt GitHub qualifiers. Structured filters are also appended into the final `q` search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowForking": true,
      "archived": true,
      "archiveUrl": "https://example.com",
      "assigneesUrl": "https://example.com",
      "blobsUrl": "https://example.com",
      "branchesUrl": "https://example.com",
      "cloneUrl": "https://example.com",
      "collaboratorsUrl": "https://example.com",
      "commentsUrl": "https://example.com",
      "commitsUrl": "https://example.com",
      "compareUrl": "https://example.com",
      "contentsUrl": "https://example.com",
      "contributorsUrl": "https://example.com",
      "createdAt": "string",
      "defaultBranch": "string",
      "deploymentsUrl": "https://example.com",
      "description": "string",
      "disabled": true,
      "downloadsUrl": "https://example.com",
      "eventsUrl": "https://example.com",
      "fork": true,
      "forks": 1,
      "forksCount": 1,
      "forksUrl": "https://example.com",
      "fullName": "Ava Chen",
      "gitCommitsUrl": "https://example.com",
      "gitRefsUrl": "https://example.com",
      "gitTagsUrl": "https://example.com",
      "gitUrl": "https://example.com",
      "hasDiscussions": true,
      "hasDownloads": true,
      "hasIssues": true,
      "hasPages": true,
      "hasProjects": true,
      "hasPullRequests": true,
      "hasWiki": true,
      "homepage": "string",
      "hooksUrl": "https://example.com",
      "htmlUrl": "https://example.com",
      "id": 1,
      "issueCommentUrl": "https://example.com",
      "issueEventsUrl": "https://example.com",
      "issuesUrl": "https://example.com",
      "isTemplate": true,
      "keysUrl": "https://example.com",
      "labelsUrl": "https://example.com",
      "language": "string",
      "languagesUrl": "https://example.com",
      "license": {},
      "mergesUrl": "https://example.com",
      "milestonesUrl": "https://example.com",
      "mirrorUrl": {},
      "name": "Ava Chen",
      "nodeId": "string",
      "notificationsUrl": "https://example.com",
      "openIssues": 1,
      "openIssuesCount": 1,
      "owner": {
        "avatarUrl": "https://example.com",
        "eventsUrl": "https://example.com",
        "followersUrl": "https://example.com",
        "followingUrl": "https://example.com",
        "gistsUrl": "https://example.com",
        "gravatarId": "string",
        "htmlUrl": "https://example.com",
        "id": 1,
        "login": "string",
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
      },
      "permissions": {
        "admin": true,
        "maintain": true,
        "pull": true,
        "push": true,
        "triage": true
      },
      "private": true,
      "pullRequestCreationPolicy": "string",
      "pullsUrl": "https://example.com",
      "pushedAt": "string",
      "releasesUrl": "https://example.com",
      "score": 1,
      "size": 1,
      "sshUrl": "https://example.com",
      "stargazersCount": 1,
      "stargazersUrl": "https://example.com",
      "statusesUrl": "https://example.com",
      "subscribersUrl": "https://example.com",
      "subscriptionUrl": "https://example.com",
      "svnUrl": "https://example.com",
      "tagsUrl": "https://example.com",
      "teamsUrl": "https://example.com",
      "topics": [
        "string"
      ],
      "treesUrl": "https://example.com",
      "updatedAt": "string",
      "url": "https://example.com",
      "visibility": "string",
      "watchers": 1,
      "watchersCount": 1,
      "webCommitSignoffRequired": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowForking` | boolean |  |
| `archived` | boolean |  |
| `archiveUrl` | string |  |
| `assigneesUrl` | string |  |
| `blobsUrl` | string |  |
| `branchesUrl` | string |  |
| `cloneUrl` | string |  |
| `collaboratorsUrl` | string |  |
| `commentsUrl` | string |  |
| `commitsUrl` | string |  |
| `compareUrl` | string |  |
| `contentsUrl` | string |  |
| `contributorsUrl` | string |  |
| `createdAt` | string |  |
| `defaultBranch` | string |  |
| `deploymentsUrl` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `downloadsUrl` | string |  |
| `eventsUrl` | string |  |
| `fork` | boolean |  |
| `forks` | number |  |
| `forksCount` | number |  |
| `forksUrl` | string |  |
| `fullName` | string |  |
| `gitCommitsUrl` | string |  |
| `gitRefsUrl` | string |  |
| `gitTagsUrl` | string |  |
| `gitUrl` | string |  |
| `hasDiscussions` | boolean |  |
| `hasDownloads` | boolean |  |
| `hasIssues` | boolean |  |
| `hasPages` | boolean |  |
| `hasProjects` | boolean |  |
| `hasPullRequests` | boolean |  |
| `hasWiki` | boolean |  |
| `homepage` | string |  |
| `hooksUrl` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `issueCommentUrl` | string |  |
| `issueEventsUrl` | string |  |
| `issuesUrl` | string |  |
| `isTemplate` | boolean |  |
| `keysUrl` | string |  |
| `labelsUrl` | string |  |
| `language` | string |  |
| `languagesUrl` | string |  |
| `license` | object |  |
| `mergesUrl` | string |  |
| `milestonesUrl` | string |  |
| `mirrorUrl` | object |  |
| `name` | string |  |
| `nodeId` | string |  |
| `notificationsUrl` | string |  |
| `openIssues` | number |  |
| `openIssuesCount` | number |  |
| `owner.avatarUrl` | string |  |
| `owner.eventsUrl` | string |  |
| `owner.followersUrl` | string |  |
| `owner.followingUrl` | string |  |
| `owner.gistsUrl` | string |  |
| `owner.gravatarId` | string |  |
| `owner.htmlUrl` | string |  |
| `owner.id` | number |  |
| `owner.login` | string |  |
| `owner.nodeId` | string |  |
| `owner.organizationsUrl` | string |  |
| `owner.receivedEventsUrl` | string |  |
| `owner.reposUrl` | string |  |
| `owner.siteAdmin` | boolean |  |
| `owner.starredUrl` | string |  |
| `owner.subscriptionsUrl` | string |  |
| `owner.type` | string |  |
| `owner.url` | string |  |
| `owner.userViewType` | string |  |
| `permissions.admin` | boolean |  |
| `permissions.maintain` | boolean |  |
| `permissions.pull` | boolean |  |
| `permissions.push` | boolean |  |
| `permissions.triage` | boolean |  |
| `private` | boolean |  |
| `pullRequestCreationPolicy` | string |  |
| `pullsUrl` | string |  |
| `pushedAt` | string |  |
| `releasesUrl` | string |  |
| `score` | number |  |
| `size` | number |  |
| `sshUrl` | string |  |
| `stargazersCount` | number |  |
| `stargazersUrl` | string |  |
| `statusesUrl` | string |  |
| `subscribersUrl` | string |  |
| `subscriptionUrl` | string |  |
| `svnUrl` | string |  |
| `tagsUrl` | string |  |
| `teamsUrl` | string |  |
| `topics[]` | string |  |
| `treesUrl` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `visibility` | string |  |
| `watchers` | number |  |
| `watchersCount` | number |  |
| `webCommitSignoffRequired` | boolean |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /search/repositories` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-repositories.md) for the provider-specific parameters and requirements.

