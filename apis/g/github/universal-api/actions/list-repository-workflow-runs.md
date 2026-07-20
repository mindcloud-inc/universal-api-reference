# GitHub: List Repository Workflow Runs

Lists workflow runs in a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-repository-workflow-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-repository-workflow-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-repository-workflow-runs?${params}`, {
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
| `actor` | string | no | Return workflow runs for the specified actor login. |
| `branch` | string | no | Return workflow runs associated with a branch name. |
| `event` | string | no | Return workflow runs triggered by the specified event. |
| `status` | string | no | Return workflow runs with the specified status or conclusion. |
| `created` | string | no | Return workflow runs created within the specified date-time range syntax. |
| `exclude_pull_requests` | boolean | no | If true, omit pull requests from the response. |
| `check_suite_id` | number | no | Return workflow runs with the specified check suite ID. |
| `head_sha` | string | no | Only return workflow runs associated with the specified head SHA. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actor": {
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
      "artifactsUrl": "https://example.com",
      "cancelUrl": "https://example.com",
      "checkSuiteId": 1,
      "checkSuiteNodeId": "string",
      "checkSuiteUrl": "https://example.com",
      "conclusion": "string",
      "createdAt": "string",
      "displayTitle": "string",
      "event": "string",
      "headBranch": "string",
      "headCommit": {
        "author": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "committer": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "id": "string",
        "message": "string",
        "timestamp": "string",
        "treeId": "string"
      },
      "headRepository": {
        "archiveUrl": "https://example.com",
        "assigneesUrl": "https://example.com",
        "blobsUrl": "https://example.com",
        "branchesUrl": "https://example.com",
        "collaboratorsUrl": "https://example.com",
        "commentsUrl": "https://example.com",
        "commitsUrl": "https://example.com",
        "compareUrl": "https://example.com",
        "contentsUrl": "https://example.com",
        "contributorsUrl": "https://example.com",
        "deploymentsUrl": "https://example.com",
        "description": "string",
        "downloadsUrl": "https://example.com",
        "eventsUrl": "https://example.com",
        "fork": true,
        "forksUrl": "https://example.com",
        "fullName": "Ava Chen",
        "gitCommitsUrl": "https://example.com",
        "gitRefsUrl": "https://example.com",
        "gitTagsUrl": "https://example.com",
        "hooksUrl": "https://example.com",
        "htmlUrl": "https://example.com",
        "id": 1,
        "issueCommentUrl": "https://example.com",
        "issueEventsUrl": "https://example.com",
        "issuesUrl": "https://example.com",
        "keysUrl": "https://example.com",
        "labelsUrl": "https://example.com",
        "languagesUrl": "https://example.com",
        "mergesUrl": "https://example.com",
        "milestonesUrl": "https://example.com",
        "name": "Ava Chen",
        "nodeId": "string",
        "notificationsUrl": "https://example.com",
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
        "private": true,
        "pullsUrl": "https://example.com",
        "releasesUrl": "https://example.com",
        "stargazersUrl": "https://example.com",
        "statusesUrl": "https://example.com",
        "subscribersUrl": "https://example.com",
        "subscriptionUrl": "https://example.com",
        "tagsUrl": "https://example.com",
        "teamsUrl": "https://example.com",
        "treesUrl": "https://example.com",
        "url": "https://example.com"
      },
      "headSha": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "jobsUrl": "https://example.com",
      "logsUrl": "https://example.com",
      "name": "Ava Chen",
      "nodeId": "string",
      "path": "string",
      "previousAttemptUrl": {},
      "pullRequests": [
        {
          "base": {
            "ref": "string",
            "repo": {
              "id": 1,
              "name": "Ava Chen",
              "url": "https://example.com"
            },
            "sha": "string"
          },
          "head": {
            "ref": "string",
            "repo": {
              "id": 1,
              "name": "Ava Chen",
              "url": "https://example.com"
            },
            "sha": "string"
          },
          "id": 1,
          "number": 1,
          "url": "https://example.com"
        }
      ],
      "referencedWorkflows": [
        {
          "path": "string",
          "ref": "string",
          "sha": "string"
        }
      ],
      "repository": {
        "archiveUrl": "https://example.com",
        "assigneesUrl": "https://example.com",
        "blobsUrl": "https://example.com",
        "branchesUrl": "https://example.com",
        "collaboratorsUrl": "https://example.com",
        "commentsUrl": "https://example.com",
        "commitsUrl": "https://example.com",
        "compareUrl": "https://example.com",
        "contentsUrl": "https://example.com",
        "contributorsUrl": "https://example.com",
        "deploymentsUrl": "https://example.com",
        "description": "string",
        "downloadsUrl": "https://example.com",
        "eventsUrl": "https://example.com",
        "fork": true,
        "forksUrl": "https://example.com",
        "fullName": "Ava Chen",
        "gitCommitsUrl": "https://example.com",
        "gitRefsUrl": "https://example.com",
        "gitTagsUrl": "https://example.com",
        "hooksUrl": "https://example.com",
        "htmlUrl": "https://example.com",
        "id": 1,
        "issueCommentUrl": "https://example.com",
        "issueEventsUrl": "https://example.com",
        "issuesUrl": "https://example.com",
        "keysUrl": "https://example.com",
        "labelsUrl": "https://example.com",
        "languagesUrl": "https://example.com",
        "mergesUrl": "https://example.com",
        "milestonesUrl": "https://example.com",
        "name": "Ava Chen",
        "nodeId": "string",
        "notificationsUrl": "https://example.com",
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
        "private": true,
        "pullsUrl": "https://example.com",
        "releasesUrl": "https://example.com",
        "stargazersUrl": "https://example.com",
        "statusesUrl": "https://example.com",
        "subscribersUrl": "https://example.com",
        "subscriptionUrl": "https://example.com",
        "tagsUrl": "https://example.com",
        "teamsUrl": "https://example.com",
        "treesUrl": "https://example.com",
        "url": "https://example.com"
      },
      "rerunUrl": "https://example.com",
      "runAttempt": 1,
      "runNumber": 1,
      "runStartedAt": "string",
      "status": "string",
      "triggeringActor": {
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
      "updatedAt": "string",
      "url": "https://example.com",
      "workflowId": 1,
      "workflowUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor.avatarUrl` | string |  |
| `actor.eventsUrl` | string |  |
| `actor.followersUrl` | string |  |
| `actor.followingUrl` | string |  |
| `actor.gistsUrl` | string |  |
| `actor.gravatarId` | string |  |
| `actor.htmlUrl` | string |  |
| `actor.id` | number |  |
| `actor.login` | string |  |
| `actor.nodeId` | string |  |
| `actor.organizationsUrl` | string |  |
| `actor.receivedEventsUrl` | string |  |
| `actor.reposUrl` | string |  |
| `actor.siteAdmin` | boolean |  |
| `actor.starredUrl` | string |  |
| `actor.subscriptionsUrl` | string |  |
| `actor.type` | string |  |
| `actor.url` | string |  |
| `actor.userViewType` | string |  |
| `artifactsUrl` | string |  |
| `cancelUrl` | string |  |
| `checkSuiteId` | number |  |
| `checkSuiteNodeId` | string |  |
| `checkSuiteUrl` | string |  |
| `conclusion` | string |  |
| `createdAt` | string |  |
| `displayTitle` | string |  |
| `event` | string |  |
| `headBranch` | string |  |
| `headCommit.author.email` | string |  |
| `headCommit.author.name` | string |  |
| `headCommit.committer.email` | string |  |
| `headCommit.committer.name` | string |  |
| `headCommit.id` | string |  |
| `headCommit.message` | string |  |
| `headCommit.timestamp` | string |  |
| `headCommit.treeId` | string |  |
| `headRepository.archiveUrl` | string |  |
| `headRepository.assigneesUrl` | string |  |
| `headRepository.blobsUrl` | string |  |
| `headRepository.branchesUrl` | string |  |
| `headRepository.collaboratorsUrl` | string |  |
| `headRepository.commentsUrl` | string |  |
| `headRepository.commitsUrl` | string |  |
| `headRepository.compareUrl` | string |  |
| `headRepository.contentsUrl` | string |  |
| `headRepository.contributorsUrl` | string |  |
| `headRepository.deploymentsUrl` | string |  |
| `headRepository.description` | string |  |
| `headRepository.downloadsUrl` | string |  |
| `headRepository.eventsUrl` | string |  |
| `headRepository.fork` | boolean |  |
| `headRepository.forksUrl` | string |  |
| `headRepository.fullName` | string |  |
| `headRepository.gitCommitsUrl` | string |  |
| `headRepository.gitRefsUrl` | string |  |
| `headRepository.gitTagsUrl` | string |  |
| `headRepository.hooksUrl` | string |  |
| `headRepository.htmlUrl` | string |  |
| `headRepository.id` | number |  |
| `headRepository.issueCommentUrl` | string |  |
| `headRepository.issueEventsUrl` | string |  |
| `headRepository.issuesUrl` | string |  |
| `headRepository.keysUrl` | string |  |
| `headRepository.labelsUrl` | string |  |
| `headRepository.languagesUrl` | string |  |
| `headRepository.mergesUrl` | string |  |
| `headRepository.milestonesUrl` | string |  |
| `headRepository.name` | string |  |
| `headRepository.nodeId` | string |  |
| `headRepository.notificationsUrl` | string |  |
| `headRepository.owner.avatarUrl` | string |  |
| `headRepository.owner.eventsUrl` | string |  |
| `headRepository.owner.followersUrl` | string |  |
| `headRepository.owner.followingUrl` | string |  |
| `headRepository.owner.gistsUrl` | string |  |
| `headRepository.owner.gravatarId` | string |  |
| `headRepository.owner.htmlUrl` | string |  |
| `headRepository.owner.id` | number |  |
| `headRepository.owner.login` | string |  |
| `headRepository.owner.nodeId` | string |  |
| `headRepository.owner.organizationsUrl` | string |  |
| `headRepository.owner.receivedEventsUrl` | string |  |
| `headRepository.owner.reposUrl` | string |  |
| `headRepository.owner.siteAdmin` | boolean |  |
| `headRepository.owner.starredUrl` | string |  |
| `headRepository.owner.subscriptionsUrl` | string |  |
| `headRepository.owner.type` | string |  |
| `headRepository.owner.url` | string |  |
| `headRepository.owner.userViewType` | string |  |
| `headRepository.private` | boolean |  |
| `headRepository.pullsUrl` | string |  |
| `headRepository.releasesUrl` | string |  |
| `headRepository.stargazersUrl` | string |  |
| `headRepository.statusesUrl` | string |  |
| `headRepository.subscribersUrl` | string |  |
| `headRepository.subscriptionUrl` | string |  |
| `headRepository.tagsUrl` | string |  |
| `headRepository.teamsUrl` | string |  |
| `headRepository.treesUrl` | string |  |
| `headRepository.url` | string |  |
| `headSha` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `jobsUrl` | string |  |
| `logsUrl` | string |  |
| `name` | string |  |
| `nodeId` | string |  |
| `path` | string |  |
| `previousAttemptUrl` | object |  |
| `pullRequests[].base.ref` | string |  |
| `pullRequests[].base.repo.id` | number |  |
| `pullRequests[].base.repo.name` | string |  |
| `pullRequests[].base.repo.url` | string |  |
| `pullRequests[].base.sha` | string |  |
| `pullRequests[].head.ref` | string |  |
| `pullRequests[].head.repo.id` | number |  |
| `pullRequests[].head.repo.name` | string |  |
| `pullRequests[].head.repo.url` | string |  |
| `pullRequests[].head.sha` | string |  |
| `pullRequests[].id` | number |  |
| `pullRequests[].number` | number |  |
| `pullRequests[].url` | string |  |
| `referencedWorkflows[].path` | string |  |
| `referencedWorkflows[].ref` | string |  |
| `referencedWorkflows[].sha` | string |  |
| `repository.archiveUrl` | string |  |
| `repository.assigneesUrl` | string |  |
| `repository.blobsUrl` | string |  |
| `repository.branchesUrl` | string |  |
| `repository.collaboratorsUrl` | string |  |
| `repository.commentsUrl` | string |  |
| `repository.commitsUrl` | string |  |
| `repository.compareUrl` | string |  |
| `repository.contentsUrl` | string |  |
| `repository.contributorsUrl` | string |  |
| `repository.deploymentsUrl` | string |  |
| `repository.description` | string |  |
| `repository.downloadsUrl` | string |  |
| `repository.eventsUrl` | string |  |
| `repository.fork` | boolean |  |
| `repository.forksUrl` | string |  |
| `repository.fullName` | string |  |
| `repository.gitCommitsUrl` | string |  |
| `repository.gitRefsUrl` | string |  |
| `repository.gitTagsUrl` | string |  |
| `repository.hooksUrl` | string |  |
| `repository.htmlUrl` | string |  |
| `repository.id` | number |  |
| `repository.issueCommentUrl` | string |  |
| `repository.issueEventsUrl` | string |  |
| `repository.issuesUrl` | string |  |
| `repository.keysUrl` | string |  |
| `repository.labelsUrl` | string |  |
| `repository.languagesUrl` | string |  |
| `repository.mergesUrl` | string |  |
| `repository.milestonesUrl` | string |  |
| `repository.name` | string |  |
| `repository.nodeId` | string |  |
| `repository.notificationsUrl` | string |  |
| `repository.owner.avatarUrl` | string |  |
| `repository.owner.eventsUrl` | string |  |
| `repository.owner.followersUrl` | string |  |
| `repository.owner.followingUrl` | string |  |
| `repository.owner.gistsUrl` | string |  |
| `repository.owner.gravatarId` | string |  |
| `repository.owner.htmlUrl` | string |  |
| `repository.owner.id` | number |  |
| `repository.owner.login` | string |  |
| `repository.owner.nodeId` | string |  |
| `repository.owner.organizationsUrl` | string |  |
| `repository.owner.receivedEventsUrl` | string |  |
| `repository.owner.reposUrl` | string |  |
| `repository.owner.siteAdmin` | boolean |  |
| `repository.owner.starredUrl` | string |  |
| `repository.owner.subscriptionsUrl` | string |  |
| `repository.owner.type` | string |  |
| `repository.owner.url` | string |  |
| `repository.owner.userViewType` | string |  |
| `repository.private` | boolean |  |
| `repository.pullsUrl` | string |  |
| `repository.releasesUrl` | string |  |
| `repository.stargazersUrl` | string |  |
| `repository.statusesUrl` | string |  |
| `repository.subscribersUrl` | string |  |
| `repository.subscriptionUrl` | string |  |
| `repository.tagsUrl` | string |  |
| `repository.teamsUrl` | string |  |
| `repository.treesUrl` | string |  |
| `repository.url` | string |  |
| `rerunUrl` | string |  |
| `runAttempt` | number |  |
| `runNumber` | number |  |
| `runStartedAt` | string |  |
| `status` | string |  |
| `triggeringActor.avatarUrl` | string |  |
| `triggeringActor.eventsUrl` | string |  |
| `triggeringActor.followersUrl` | string |  |
| `triggeringActor.followingUrl` | string |  |
| `triggeringActor.gistsUrl` | string |  |
| `triggeringActor.gravatarId` | string |  |
| `triggeringActor.htmlUrl` | string |  |
| `triggeringActor.id` | number |  |
| `triggeringActor.login` | string |  |
| `triggeringActor.nodeId` | string |  |
| `triggeringActor.organizationsUrl` | string |  |
| `triggeringActor.receivedEventsUrl` | string |  |
| `triggeringActor.reposUrl` | string |  |
| `triggeringActor.siteAdmin` | boolean |  |
| `triggeringActor.starredUrl` | string |  |
| `triggeringActor.subscriptionsUrl` | string |  |
| `triggeringActor.type` | string |  |
| `triggeringActor.url` | string |  |
| `triggeringActor.userViewType` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `workflowId` | number |  |
| `workflowUrl` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/actions/runs` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-repository-workflow-runs.md) for the provider-specific parameters and requirements.

