# GitHub: Request Pull Request Reviewers

Requests reviews from users or teams on a GitHub pull request.

```
POST https://connect.mindcloud.co/v1/universal/github/latest/actions/request-pull-request-reviewers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/github/latest/actions/request-pull-request-reviewers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "pullNumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/request-pull-request-reviewers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "pullNumber": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | string | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `pullNumber` | number | yes | The number that identifies the pull request. |
| `reviewers` | array<string> | no | User logins that will be requested as reviewers. Example: `octocat`. |
| `teamReviewers` | array<string> | no | Team slugs that will be requested as reviewers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "title": "string",
      "number": 1,
      "state": "string",
      "htmlUrl": "https://example.com",
      "draft": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "closedAt": "2026-05-07T12:00:00.000Z",
      "mergedAt": "2026-05-07T12:00:00.000Z",
      "body": "string",
      "id": 1,
      "activeLockReason": "string",
      "assignee": {
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
      },
      "assignees": [
        {
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
      ],
      "authorAssociation": "string",
      "autoMerge": {},
      "base": {
        "label": "string",
        "ref": "string",
        "repo": {
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
          "createdAt": "2026-05-07T12:00:00.000Z",
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
          "mirrorUrl": "https://example.com",
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
          },
          "private": true,
          "pullRequestCreationPolicy": "string",
          "pullsUrl": "https://example.com",
          "pushedAt": "2026-05-07T12:00:00.000Z",
          "releasesUrl": "https://example.com",
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
          "treesUrl": "https://example.com",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com",
          "visibility": "string",
          "watchers": 1,
          "watchersCount": 1,
          "webCommitSignoffRequired": true
        },
        "sha": "string",
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
      },
      "commentsUrl": "https://example.com",
      "commitsUrl": "https://example.com",
      "diffUrl": "https://example.com",
      "head": {
        "label": "string",
        "ref": "string",
        "repo": {
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
          "createdAt": "2026-05-07T12:00:00.000Z",
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
          "mirrorUrl": "https://example.com",
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
          },
          "private": true,
          "pullRequestCreationPolicy": "string",
          "pullsUrl": "https://example.com",
          "pushedAt": "2026-05-07T12:00:00.000Z",
          "releasesUrl": "https://example.com",
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
          "treesUrl": "https://example.com",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com",
          "visibility": "string",
          "watchers": 1,
          "watchersCount": 1,
          "webCommitSignoffRequired": true
        },
        "sha": "string",
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
      },
      "issueUrl": "https://example.com",
      "labels": [
        {
          "archivedAt": "2026-05-07T12:00:00.000Z",
          "archivedBy": {},
          "color": "string",
          "default": true,
          "description": "string",
          "id": 1,
          "name": "Ava Chen",
          "nodeId": "string",
          "url": "https://example.com"
        }
      ],
      "Links": {
        "comments": {
          "href": "https://example.com"
        },
        "commits": {
          "href": "https://example.com"
        },
        "html": {
          "href": "https://example.com"
        },
        "issue": {
          "href": "https://example.com"
        },
        "reviewComment": {
          "href": "https://example.com"
        },
        "reviewComments": {
          "href": "https://example.com"
        },
        "self": {
          "href": "https://example.com"
        },
        "statuses": {
          "href": "https://example.com"
        }
      },
      "locked": true,
      "mergeCommitSha": "string",
      "milestone": {},
      "nodeId": "string",
      "patchUrl": "https://example.com",
      "reviewCommentsUrl": "https://example.com",
      "reviewCommentUrl": "https://example.com",
      "statusesUrl": "https://example.com",
      "url": "https://example.com",
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
| `title` | string |  |
| `number` | number |  |
| `state` | string |  |
| `htmlUrl` | string |  |
| `draft` | boolean |  |
| `createdAt` | date |  |
| `updatedAt` | date |  |
| `closedAt` | date |  |
| `mergedAt` | date |  |
| `body` | string |  |
| `id` | number |  |
| `activeLockReason` | string |  |
| `assignee.avatarUrl` | string |  |
| `assignee.eventsUrl` | string |  |
| `assignee.followersUrl` | string |  |
| `assignee.followingUrl` | string |  |
| `assignee.gistsUrl` | string |  |
| `assignee.gravatarId` | string |  |
| `assignee.htmlUrl` | string |  |
| `assignee.id` | number |  |
| `assignee.login` | string |  |
| `assignee.nodeId` | string |  |
| `assignee.organizationsUrl` | string |  |
| `assignee.receivedEventsUrl` | string |  |
| `assignee.reposUrl` | string |  |
| `assignee.siteAdmin` | boolean |  |
| `assignee.starredUrl` | string |  |
| `assignee.subscriptionsUrl` | string |  |
| `assignee.type` | string |  |
| `assignee.url` | string |  |
| `assignee.userViewType` | string |  |
| `assignees[].avatarUrl` | string |  |
| `assignees[].eventsUrl` | string |  |
| `assignees[].followersUrl` | string |  |
| `assignees[].followingUrl` | string |  |
| `assignees[].gistsUrl` | string |  |
| `assignees[].gravatarId` | string |  |
| `assignees[].htmlUrl` | string |  |
| `assignees[].id` | number |  |
| `assignees[].login` | string |  |
| `assignees[].nodeId` | string |  |
| `assignees[].organizationsUrl` | string |  |
| `assignees[].receivedEventsUrl` | string |  |
| `assignees[].reposUrl` | string |  |
| `assignees[].siteAdmin` | boolean |  |
| `assignees[].starredUrl` | string |  |
| `assignees[].subscriptionsUrl` | string |  |
| `assignees[].type` | string |  |
| `assignees[].url` | string |  |
| `assignees[].userViewType` | string |  |
| `authorAssociation` | string |  |
| `autoMerge` | object |  |
| `base.label` | string |  |
| `base.ref` | string |  |
| `base.repo.allowForking` | boolean |  |
| `base.repo.archived` | boolean |  |
| `base.repo.archiveUrl` | string |  |
| `base.repo.assigneesUrl` | string |  |
| `base.repo.blobsUrl` | string |  |
| `base.repo.branchesUrl` | string |  |
| `base.repo.cloneUrl` | string |  |
| `base.repo.collaboratorsUrl` | string |  |
| `base.repo.commentsUrl` | string |  |
| `base.repo.commitsUrl` | string |  |
| `base.repo.compareUrl` | string |  |
| `base.repo.contentsUrl` | string |  |
| `base.repo.contributorsUrl` | string |  |
| `base.repo.createdAt` | date |  |
| `base.repo.defaultBranch` | string |  |
| `base.repo.deploymentsUrl` | string |  |
| `base.repo.description` | string |  |
| `base.repo.disabled` | boolean |  |
| `base.repo.downloadsUrl` | string |  |
| `base.repo.eventsUrl` | string |  |
| `base.repo.fork` | boolean |  |
| `base.repo.forks` | number |  |
| `base.repo.forksCount` | number |  |
| `base.repo.forksUrl` | string |  |
| `base.repo.fullName` | string |  |
| `base.repo.gitCommitsUrl` | string |  |
| `base.repo.gitRefsUrl` | string |  |
| `base.repo.gitTagsUrl` | string |  |
| `base.repo.gitUrl` | string |  |
| `base.repo.hasDiscussions` | boolean |  |
| `base.repo.hasDownloads` | boolean |  |
| `base.repo.hasIssues` | boolean |  |
| `base.repo.hasPages` | boolean |  |
| `base.repo.hasProjects` | boolean |  |
| `base.repo.hasPullRequests` | boolean |  |
| `base.repo.hasWiki` | boolean |  |
| `base.repo.homepage` | string |  |
| `base.repo.hooksUrl` | string |  |
| `base.repo.htmlUrl` | string |  |
| `base.repo.id` | number |  |
| `base.repo.issueCommentUrl` | string |  |
| `base.repo.issueEventsUrl` | string |  |
| `base.repo.issuesUrl` | string |  |
| `base.repo.isTemplate` | boolean |  |
| `base.repo.keysUrl` | string |  |
| `base.repo.labelsUrl` | string |  |
| `base.repo.language` | string |  |
| `base.repo.languagesUrl` | string |  |
| `base.repo.license` | object |  |
| `base.repo.mergesUrl` | string |  |
| `base.repo.milestonesUrl` | string |  |
| `base.repo.mirrorUrl` | string |  |
| `base.repo.name` | string |  |
| `base.repo.nodeId` | string |  |
| `base.repo.notificationsUrl` | string |  |
| `base.repo.openIssues` | number |  |
| `base.repo.openIssuesCount` | number |  |
| `base.repo.owner.avatarUrl` | string |  |
| `base.repo.owner.eventsUrl` | string |  |
| `base.repo.owner.followersUrl` | string |  |
| `base.repo.owner.followingUrl` | string |  |
| `base.repo.owner.gistsUrl` | string |  |
| `base.repo.owner.gravatarId` | string |  |
| `base.repo.owner.htmlUrl` | string |  |
| `base.repo.owner.id` | number |  |
| `base.repo.owner.login` | string |  |
| `base.repo.owner.nodeId` | string |  |
| `base.repo.owner.organizationsUrl` | string |  |
| `base.repo.owner.receivedEventsUrl` | string |  |
| `base.repo.owner.reposUrl` | string |  |
| `base.repo.owner.siteAdmin` | boolean |  |
| `base.repo.owner.starredUrl` | string |  |
| `base.repo.owner.subscriptionsUrl` | string |  |
| `base.repo.owner.type` | string |  |
| `base.repo.owner.url` | string |  |
| `base.repo.owner.userViewType` | string |  |
| `base.repo.private` | boolean |  |
| `base.repo.pullRequestCreationPolicy` | string |  |
| `base.repo.pullsUrl` | string |  |
| `base.repo.pushedAt` | date |  |
| `base.repo.releasesUrl` | string |  |
| `base.repo.size` | number |  |
| `base.repo.sshUrl` | string |  |
| `base.repo.stargazersCount` | number |  |
| `base.repo.stargazersUrl` | string |  |
| `base.repo.statusesUrl` | string |  |
| `base.repo.subscribersUrl` | string |  |
| `base.repo.subscriptionUrl` | string |  |
| `base.repo.svnUrl` | string |  |
| `base.repo.tagsUrl` | string |  |
| `base.repo.teamsUrl` | string |  |
| `base.repo.treesUrl` | string |  |
| `base.repo.updatedAt` | date |  |
| `base.repo.url` | string |  |
| `base.repo.visibility` | string |  |
| `base.repo.watchers` | number |  |
| `base.repo.watchersCount` | number |  |
| `base.repo.webCommitSignoffRequired` | boolean |  |
| `base.sha` | string |  |
| `base.user.avatarUrl` | string |  |
| `base.user.eventsUrl` | string |  |
| `base.user.followersUrl` | string |  |
| `base.user.followingUrl` | string |  |
| `base.user.gistsUrl` | string |  |
| `base.user.gravatarId` | string |  |
| `base.user.htmlUrl` | string |  |
| `base.user.id` | number |  |
| `base.user.login` | string |  |
| `base.user.nodeId` | string |  |
| `base.user.organizationsUrl` | string |  |
| `base.user.receivedEventsUrl` | string |  |
| `base.user.reposUrl` | string |  |
| `base.user.siteAdmin` | boolean |  |
| `base.user.starredUrl` | string |  |
| `base.user.subscriptionsUrl` | string |  |
| `base.user.type` | string |  |
| `base.user.url` | string |  |
| `base.user.userViewType` | string |  |
| `commentsUrl` | string |  |
| `commitsUrl` | string |  |
| `diffUrl` | string |  |
| `head.label` | string |  |
| `head.ref` | string |  |
| `head.repo.allowForking` | boolean |  |
| `head.repo.archived` | boolean |  |
| `head.repo.archiveUrl` | string |  |
| `head.repo.assigneesUrl` | string |  |
| `head.repo.blobsUrl` | string |  |
| `head.repo.branchesUrl` | string |  |
| `head.repo.cloneUrl` | string |  |
| `head.repo.collaboratorsUrl` | string |  |
| `head.repo.commentsUrl` | string |  |
| `head.repo.commitsUrl` | string |  |
| `head.repo.compareUrl` | string |  |
| `head.repo.contentsUrl` | string |  |
| `head.repo.contributorsUrl` | string |  |
| `head.repo.createdAt` | date |  |
| `head.repo.defaultBranch` | string |  |
| `head.repo.deploymentsUrl` | string |  |
| `head.repo.description` | string |  |
| `head.repo.disabled` | boolean |  |
| `head.repo.downloadsUrl` | string |  |
| `head.repo.eventsUrl` | string |  |
| `head.repo.fork` | boolean |  |
| `head.repo.forks` | number |  |
| `head.repo.forksCount` | number |  |
| `head.repo.forksUrl` | string |  |
| `head.repo.fullName` | string |  |
| `head.repo.gitCommitsUrl` | string |  |
| `head.repo.gitRefsUrl` | string |  |
| `head.repo.gitTagsUrl` | string |  |
| `head.repo.gitUrl` | string |  |
| `head.repo.hasDiscussions` | boolean |  |
| `head.repo.hasDownloads` | boolean |  |
| `head.repo.hasIssues` | boolean |  |
| `head.repo.hasPages` | boolean |  |
| `head.repo.hasProjects` | boolean |  |
| `head.repo.hasPullRequests` | boolean |  |
| `head.repo.hasWiki` | boolean |  |
| `head.repo.homepage` | string |  |
| `head.repo.hooksUrl` | string |  |
| `head.repo.htmlUrl` | string |  |
| `head.repo.id` | number |  |
| `head.repo.issueCommentUrl` | string |  |
| `head.repo.issueEventsUrl` | string |  |
| `head.repo.issuesUrl` | string |  |
| `head.repo.isTemplate` | boolean |  |
| `head.repo.keysUrl` | string |  |
| `head.repo.labelsUrl` | string |  |
| `head.repo.language` | string |  |
| `head.repo.languagesUrl` | string |  |
| `head.repo.license` | object |  |
| `head.repo.mergesUrl` | string |  |
| `head.repo.milestonesUrl` | string |  |
| `head.repo.mirrorUrl` | string |  |
| `head.repo.name` | string |  |
| `head.repo.nodeId` | string |  |
| `head.repo.notificationsUrl` | string |  |
| `head.repo.openIssues` | number |  |
| `head.repo.openIssuesCount` | number |  |
| `head.repo.owner.avatarUrl` | string |  |
| `head.repo.owner.eventsUrl` | string |  |
| `head.repo.owner.followersUrl` | string |  |
| `head.repo.owner.followingUrl` | string |  |
| `head.repo.owner.gistsUrl` | string |  |
| `head.repo.owner.gravatarId` | string |  |
| `head.repo.owner.htmlUrl` | string |  |
| `head.repo.owner.id` | number |  |
| `head.repo.owner.login` | string |  |
| `head.repo.owner.nodeId` | string |  |
| `head.repo.owner.organizationsUrl` | string |  |
| `head.repo.owner.receivedEventsUrl` | string |  |
| `head.repo.owner.reposUrl` | string |  |
| `head.repo.owner.siteAdmin` | boolean |  |
| `head.repo.owner.starredUrl` | string |  |
| `head.repo.owner.subscriptionsUrl` | string |  |
| `head.repo.owner.type` | string |  |
| `head.repo.owner.url` | string |  |
| `head.repo.owner.userViewType` | string |  |
| `head.repo.private` | boolean |  |
| `head.repo.pullRequestCreationPolicy` | string |  |
| `head.repo.pullsUrl` | string |  |
| `head.repo.pushedAt` | date |  |
| `head.repo.releasesUrl` | string |  |
| `head.repo.size` | number |  |
| `head.repo.sshUrl` | string |  |
| `head.repo.stargazersCount` | number |  |
| `head.repo.stargazersUrl` | string |  |
| `head.repo.statusesUrl` | string |  |
| `head.repo.subscribersUrl` | string |  |
| `head.repo.subscriptionUrl` | string |  |
| `head.repo.svnUrl` | string |  |
| `head.repo.tagsUrl` | string |  |
| `head.repo.teamsUrl` | string |  |
| `head.repo.treesUrl` | string |  |
| `head.repo.updatedAt` | date |  |
| `head.repo.url` | string |  |
| `head.repo.visibility` | string |  |
| `head.repo.watchers` | number |  |
| `head.repo.watchersCount` | number |  |
| `head.repo.webCommitSignoffRequired` | boolean |  |
| `head.sha` | string |  |
| `head.user.avatarUrl` | string |  |
| `head.user.eventsUrl` | string |  |
| `head.user.followersUrl` | string |  |
| `head.user.followingUrl` | string |  |
| `head.user.gistsUrl` | string |  |
| `head.user.gravatarId` | string |  |
| `head.user.htmlUrl` | string |  |
| `head.user.id` | number |  |
| `head.user.login` | string |  |
| `head.user.nodeId` | string |  |
| `head.user.organizationsUrl` | string |  |
| `head.user.receivedEventsUrl` | string |  |
| `head.user.reposUrl` | string |  |
| `head.user.siteAdmin` | boolean |  |
| `head.user.starredUrl` | string |  |
| `head.user.subscriptionsUrl` | string |  |
| `head.user.type` | string |  |
| `head.user.url` | string |  |
| `head.user.userViewType` | string |  |
| `issueUrl` | string |  |
| `labels[].archivedAt` | date |  |
| `labels[].archivedBy` | object |  |
| `labels[].color` | string |  |
| `labels[].default` | boolean |  |
| `labels[].description` | string |  |
| `labels[].id` | number |  |
| `labels[].name` | string |  |
| `labels[].nodeId` | string |  |
| `labels[].url` | string |  |
| `Links.comments.href` | string |  |
| `Links.commits.href` | string |  |
| `Links.html.href` | string |  |
| `Links.issue.href` | string |  |
| `Links.reviewComment.href` | string |  |
| `Links.reviewComments.href` | string |  |
| `Links.self.href` | string |  |
| `Links.statuses.href` | string |  |
| `locked` | boolean |  |
| `mergeCommitSha` | string |  |
| `milestone` | object |  |
| `nodeId` | string |  |
| `patchUrl` | string |  |
| `reviewCommentsUrl` | string |  |
| `reviewCommentUrl` | string |  |
| `statusesUrl` | string |  |
| `url` | string |  |
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

Through the native GitHub API, this operation is `POST /repos/:owner/:repo/pulls/:pull_number/requested_reviewers` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-pull-request-reviewers.md) for the provider-specific parameters and requirements.

