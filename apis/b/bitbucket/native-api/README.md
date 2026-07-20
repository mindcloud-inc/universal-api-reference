# Bitbucket: Native API Reference

A consolidated summary of Bitbucket's API configuration and 52 documented operations, with links to official documentation.

- **Official docs:** https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/
- **OpenAPI specification:** https://dac-static.atlassian.com/cloud/bitbucket/swagger.v3.json?_v=2.300.162
- **API base URL:** `https://api.bitbucket.org/2.0`

## Authentication

### Bitbucket API Token (Basic)

Use the Atlassian account email as the username and the Bitbucket/Atlassian API token as the password for Bitbucket Cloud REST APIs.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.atlassian.com/cloud/bitbucket/rest/intro/#authentication)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `change_id` | path | `string` | yes | — |
| `deployment_uuid` | path | `string` | yes | — |
| `encoded_id` | path | `string` | yes | — |
| `environment_uuid` | path | `string` | yes | — |
| `filename` | path | `string` | yes | — |
| `id` | path | `string` | yes | — |
| `issue_id` | path | `string` | yes | — |
| `key_id` | path | `string` | yes | — |
| `milestone_id` | path | `string` | yes | — |
| `version_id` | path | `string` | yes | — |
| `repo_slug` | path | `string` | yes | Repository slug inside the selected Bitbucket workspace. |
| `project_key` | path | `string` | yes | Project key inside the selected Bitbucket workspace. |
| `member` | path | `string` | yes | Bitbucket account identifier for a workspace member. |
| `uid` | path | `string` | yes | Webhook identifier returned by Bitbucket. |
| `commit` | path | `string` | yes | Commit hash inside the selected repository. |
| `comment_id` | path | `string` | yes | Comment identifier returned by Bitbucket. |
| `name` | path | `string` | yes | Branch name inside the selected repository. |
| `pull_request_id` | path | `string` | yes | Pull request numeric identifier returned by Bitbucket. |
| `task_id` | path | `string` | yes | Task identifier returned by Bitbucket. |
| `pipeline_uuid` | path | `string` | yes | Pipeline UUID returned by Bitbucket. |

## Pagination

Use `pagelen` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (52 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Snippet Watching](actions/check-snippet-watching.md) | `GET /snippets/:workspace/:encoded_id/watch` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-snippets/) |
| [Create Or Update Repository](actions/create-or-update-repository.md) | `PUT /repositories/:workspace/:repo_slug` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/#api-repositories-workspace-repo-slug-put) |
| [Delete Repository](actions/delete-repository.md) | `DELETE /repositories/:workspace/:repo_slug` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/#api-repositories-workspace-repo-slug-delete) |
| [Get Branch](actions/get-branch.md) | `GET /repositories/:workspace/:repo_slug/refs/branches/:name` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-refs/) |
| [Get Branch Restriction Rule](actions/get-branch-restriction-rule.md) | `GET /repositories/:workspace/:repo_slug/branch-restrictions/:id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-branch-restrictions/) |
| [Get Commit](actions/get-commit.md) | `GET /repositories/:workspace/:repo_slug/commit/:commit` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-commits/) |
| [Get Commit Comment](actions/get-commit-comment.md) | `GET /repositories/:workspace/:repo_slug/commit/:commit/comments/:comment_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-commits/) |
| [Get Download Artifact Link](actions/get-download-artifact-link.md) | `GET /repositories/:workspace/:repo_slug/downloads/:filename` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-downloads/) |
| [Get Effective Branching Model](actions/get-effective-branching-model.md) | `GET /repositories/:workspace/:repo_slug/effective-branching-model` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-branching-model/) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /repositories/:workspace/:repo_slug/pipelines/:pipeline_uuid` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pipelines/) |
| [Get Project](actions/get-project.md) | `GET /workspaces/:workspace/projects/:project_key` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-projects/) |
| [Get Pull Request](actions/get-pull-request.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [Get Pull Request Comment](actions/get-pull-request-comment.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id/comments/:comment_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [Get Pull Request Task](actions/get-pull-request-task.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id/tasks/:task_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [Get Repository](actions/get-repository.md) | `GET /repositories/:workspace/:repo_slug` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [Get Repository Branching Model](actions/get-repository-branching-model.md) | `GET /repositories/:workspace/:repo_slug/branching-model` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-branching-model/) |
| [Get Repository Branching Model Settings](actions/get-repository-branching-model-settings.md) | `GET /repositories/:workspace/:repo_slug/branching-model/settings` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-branching-model/) |
| [Get Repository Deploy Key](actions/get-repository-deploy-key.md) | `GET /repositories/:workspace/:repo_slug/deploy-keys/:key_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-ssh/) |
| [Get Repository Settings Inheritance](actions/get-repository-settings-inheritance.md) | `GET /repositories/:workspace/:repo_slug/override-settings` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [Get Repository Webhook](actions/get-repository-webhook.md) | `GET /repositories/:workspace/:repo_slug/hooks/:uid` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [Get Snippet](actions/get-snippet.md) | `GET /snippets/:workspace/:encoded_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-snippets/) |
| [Get Snippet Comment](actions/get-snippet-comment.md) | `GET /snippets/:workspace/:encoded_id/comments/:comment_id` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-snippets/) |
| [Get Tag](actions/get-tag.md) | `GET /repositories/:workspace/:repo_slug/refs/tags/:name` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-refs/) |
| [Get User Workspace Permission](actions/get-user-workspace-permission.md) | `GET /user/workspaces/:workspace/permission` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspace` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [Get Workspace Member](actions/get-workspace-member.md) | `GET /workspaces/:workspace/members/:member` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [List Branch Restrictions](actions/list-branch-restrictions.md) | `GET /repositories/:workspace/:repo_slug/branch-restrictions` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-branch-restrictions/) |
| [List Branches](actions/list-branches.md) | `GET /repositories/:workspace/:repo_slug/refs/branches` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-refs/) |
| [List Commit Comments](actions/list-commit-comments.md) | `GET /repositories/:workspace/:repo_slug/commit/:commit/comments` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-commits/) |
| [List Commits](actions/list-commits.md) | `GET /repositories/:workspace/:repo_slug/commits` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-commits/) |
| [List My Workspaces](actions/list-my-workspaces.md) | `GET /user/workspaces` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [List Pipelines](actions/list-pipelines.md) | `GET /repositories/:workspace/:repo_slug/pipelines` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pipelines/) |
| [List Project Default Reviewers](actions/list-project-default-reviewers.md) | `GET /workspaces/:workspace/projects/:project_key/default-reviewers` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-projects/) |
| [List Projects in Workspace](actions/list-projects-in-workspace.md) | `GET /workspaces/:workspace/projects` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [List Pull Request Activity](actions/list-pull-request-activity.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id/activity` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [List Pull Request Comments](actions/list-pull-request-comments.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id/comments` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [List Pull Request Statuses](actions/list-pull-request-statuses.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id/statuses` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [List Pull Request Tasks](actions/list-pull-request-tasks.md) | `GET /repositories/:workspace/:repo_slug/pullrequests/:pull_request_id/tasks` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [List Pull Requests](actions/list-pull-requests.md) | `GET /repositories/:workspace/:repo_slug/pullrequests` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-pullrequests/) |
| [List Repositories in Workspace](actions/list-repositories-in-workspace.md) | `GET /repositories/:workspace` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [List Repository Deploy Keys](actions/list-repository-deploy-keys.md) | `GET /repositories/:workspace/:repo_slug/deploy-keys` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-ssh/) |
| [List Repository Downloads](actions/list-repository-downloads.md) | `GET /repositories/:workspace/:repo_slug/downloads` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-downloads/) |
| [List Repository Forks](actions/list-repository-forks.md) | `GET /repositories/:workspace/:repo_slug/forks` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [List Repository Watchers](actions/list-repository-watchers.md) | `GET /repositories/:workspace/:repo_slug/watchers` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [List Repository Webhooks](actions/list-repository-webhooks.md) | `GET /repositories/:workspace/:repo_slug/hooks` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/) |
| [List Snippet Comments](actions/list-snippet-comments.md) | `GET /snippets/:workspace/:encoded_id/comments` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-snippets/) |
| [List Snippet Watchers](actions/list-snippet-watchers.md) | `GET /snippets/:workspace/:encoded_id/watchers` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-snippets/) |
| [List Snippets in Workspace](actions/list-snippets-in-workspace.md) | `GET /snippets/:workspace` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-snippets/) |
| [List Tags](actions/list-tags.md) | `GET /repositories/:workspace/:repo_slug/refs/tags` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-refs/) |
| [List Workspace Members](actions/list-workspace-members.md) | `GET /workspaces/:workspace/members` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [List Workspace Permissions](actions/list-workspace-permissions.md) | `GET /workspaces/:workspace/permissions` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
| [List Workspace Repository Permissions](actions/list-workspace-repository-permissions.md) | `GET /workspaces/:workspace/permissions/repositories` | [docs](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/) |
