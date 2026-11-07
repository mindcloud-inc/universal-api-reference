# GitHub: List Check Runs for Ref

Retrieves the check runs for a commit, branch, or tag in GitHub.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-check-runs-for-ref
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-check-runs-for-ref?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string&ref=heads%2Fmain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string",
  "ref": "heads/main"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-check-runs-for-ref?${params}`, {
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
| `ref` | string | yes | A commit SHA, branch name (heads/BRANCH_NAME), or tag name (tags/TAG_NAME). Example: `heads/main`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkName` | string | no | Returns check runs with the specified name. |
| `status` | list<string> | no | Returns check runs with the specified status. One of: `completed`, `in_progress`, `queued`. |
| `filter` | list<string> | no | Filters check runs by their completed_at timestamp. latest returns the most recent check runs. One of: `all`, `latest`. Default: `latest`. |
| `appId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "status": "string",
      "conclusion": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "detailsUrl": "https://example.com",
      "htmlUrl": "https://example.com",
      "headSha": "string",
      "id": 1,
      "app": {
        "clientId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "events": [
          "string"
        ],
        "externalUrl": "https://example.com",
        "htmlUrl": "https://example.com",
        "id": 1,
        "name": "Ava Chen",
        "nodeId": "string",
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
        "permissions": {
          "actions": "string",
          "administration": "string",
          "artifactMetadata": "string",
          "attestations": "string",
          "checks": "string",
          "codeQuality": "string",
          "contents": "string",
          "copilotRequests": "string",
          "deployments": "string",
          "discussions": "string",
          "drives": "string",
          "issues": "string",
          "mergeQueues": "string",
          "metadata": "string",
          "models": "string",
          "packages": "string",
          "pages": "string",
          "pullRequests": "string",
          "repositoryHooks": "string",
          "repositoryProjects": "string",
          "securityEvents": "string",
          "statuses": "string",
          "vulnerabilityAlerts": "string"
        },
        "slug": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "checkSuite": {
        "id": 1
      },
      "externalId": "string",
      "nodeId": "string",
      "output": {
        "annotationsCount": 1,
        "annotationsUrl": "https://example.com",
        "summary": "string",
        "text": "string",
        "title": "string"
      },
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `status` | string |  |
| `conclusion` | string |  |
| `startedAt` | date |  |
| `completedAt` | date |  |
| `detailsUrl` | string |  |
| `htmlUrl` | string |  |
| `headSha` | string |  |
| `id` | number |  |
| `app.clientId` | string |  |
| `app.createdAt` | date |  |
| `app.description` | string |  |
| `app.events[]` | string |  |
| `app.externalUrl` | string |  |
| `app.htmlUrl` | string |  |
| `app.id` | number |  |
| `app.name` | string |  |
| `app.nodeId` | string |  |
| `app.owner.avatarUrl` | string |  |
| `app.owner.eventsUrl` | string |  |
| `app.owner.followersUrl` | string |  |
| `app.owner.followingUrl` | string |  |
| `app.owner.gistsUrl` | string |  |
| `app.owner.gravatarId` | string |  |
| `app.owner.htmlUrl` | string |  |
| `app.owner.id` | number |  |
| `app.owner.login` | string |  |
| `app.owner.nodeId` | string |  |
| `app.owner.organizationsUrl` | string |  |
| `app.owner.receivedEventsUrl` | string |  |
| `app.owner.reposUrl` | string |  |
| `app.owner.siteAdmin` | boolean |  |
| `app.owner.starredUrl` | string |  |
| `app.owner.subscriptionsUrl` | string |  |
| `app.owner.type` | string |  |
| `app.owner.url` | string |  |
| `app.owner.userViewType` | string |  |
| `app.permissions.actions` | string |  |
| `app.permissions.administration` | string |  |
| `app.permissions.artifactMetadata` | string |  |
| `app.permissions.attestations` | string |  |
| `app.permissions.checks` | string |  |
| `app.permissions.codeQuality` | string |  |
| `app.permissions.contents` | string |  |
| `app.permissions.copilotRequests` | string |  |
| `app.permissions.deployments` | string |  |
| `app.permissions.discussions` | string |  |
| `app.permissions.drives` | string |  |
| `app.permissions.issues` | string |  |
| `app.permissions.mergeQueues` | string |  |
| `app.permissions.metadata` | string |  |
| `app.permissions.models` | string |  |
| `app.permissions.packages` | string |  |
| `app.permissions.pages` | string |  |
| `app.permissions.pullRequests` | string |  |
| `app.permissions.repositoryHooks` | string |  |
| `app.permissions.repositoryProjects` | string |  |
| `app.permissions.securityEvents` | string |  |
| `app.permissions.statuses` | string |  |
| `app.permissions.vulnerabilityAlerts` | string |  |
| `app.slug` | string |  |
| `app.updatedAt` | date |  |
| `checkSuite.id` | number |  |
| `externalId` | string |  |
| `nodeId` | string |  |
| `output.annotationsCount` | number |  |
| `output.annotationsUrl` | string |  |
| `output.summary` | string |  |
| `output.text` | string |  |
| `output.title` | string |  |
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
| `url` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/commits/:ref/check-runs` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-check-runs-for-ref.md) for the provider-specific parameters and requirements.

