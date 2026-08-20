# GitHub: Native API Reference

A consolidated summary of GitHub's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.github.com/en/rest
- **OpenAPI specification:** https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- **API base URL:** `https://api.github.com`

## Authentication

### GitHub OAuth

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://github.com/login/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://github.com/login/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `repo read:org user workflow`.

PKCE is enabled.

[Official authentication documentation](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/authorizing-oauth-apps)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.github+json` |
| `Content-Type` | `application/json` |
| `X-GitHub-Api-Version` | `2022-11-28` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | `POST /repos/:owner/:repo/issues` | [docs](https://docs.github.com/en/rest/issues/issues#create-an-issue) |
| [Create Issue Comment](actions/create-issue-comment.md) | `POST /repos/:owner/:repo/issues/:issue_number/comments` | [docs](https://docs.github.com/en/rest/issues/comments#create-an-issue-comment) |
| [Create or Update File Content](actions/create-or-update-file-content.md) | `PUT /repos/:owner/:repo/contents/:path` | [docs](https://docs.github.com/en/rest/repos/contents#create-or-update-file-contents) |
| [Create Pull Request](actions/create-pull-request.md) | `POST /repos/:owner/:repo/pulls` | [docs](https://docs.github.com/en/rest/pulls/pulls#create-a-pull-request) |
| [Create Release](actions/create-release.md) | `POST /repos/:owner/:repo/releases` | [docs](https://docs.github.com/en/rest/releases/releases#create-a-release) |
| [Create Repository for Authenticated User](actions/create-repository-for-authenticated-user.md) | `POST /user/repos` | [docs](https://docs.github.com/en/rest/repos/repos#create-a-repository-for-the-authenticated-user) |
| [Create Workflow Dispatch Event](actions/create-workflow-dispatch-event.md) | `POST /repos/:owner/:repo/actions/workflows/:workflow_id/dispatches` | [docs](https://docs.github.com/en/rest/actions/workflows#create-a-workflow-dispatch-event) |
| [Delete File](actions/delete-file.md) | `DELETE /repos/:owner/:repo/contents/:path` | [docs](https://docs.github.com/en/rest/repos/contents#delete-a-file) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /user` | [docs](https://docs.github.com/en/rest/users/users#get-the-authenticated-user) |
| [Get Issue](actions/get-issue.md) | `GET /repos/:owner/:repo/issues/:issue_number` | [docs](https://docs.github.com/en/rest/issues/issues#get-an-issue) |
| [Get Latest Release](actions/get-latest-release.md) | `GET /repos/:owner/:repo/releases/latest` | [docs](https://docs.github.com/en/rest/releases/releases#get-the-latest-release) |
| [Get Pull Request](actions/get-pull-request.md) | `GET /repos/:owner/:repo/pulls/:pull_number` | [docs](https://docs.github.com/en/rest/pulls/pulls#get-a-pull-request) |
| [Get Repository](actions/get-repository.md) | `GET /repos/:owner/:repo` | [docs](https://docs.github.com/en/rest/repos/repos#get-a-repository) |
| [Get Repository Content](actions/get-repository-content.md) | `GET /repos/:owner/:repo/contents/:path` | [docs](https://docs.github.com/en/rest/repos/contents#get-repository-content) |
| [Get Workflow Run](actions/get-workflow-run.md) | `GET /repos/:owner/:repo/actions/runs/:run_id` | [docs](https://docs.github.com/en/rest/actions/workflow-runs#get-a-workflow-run) |
| [List Authenticated User Organizations](actions/list-authenticated-user-organizations.md) | `GET /user/orgs` | [docs](https://docs.github.com/en/rest/orgs/orgs?apiVersion=2022-11-28#list-organizations-for-the-authenticated-user) |
| [List Authenticated User Repositories](actions/list-authenticated-user-repositories.md) | `GET /user/repos` | [docs](https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#list-repositories-for-the-authenticated-user) |
| [List Branches](actions/list-branches.md) | `GET /repos/:owner/:repo/branches` | [docs](https://docs.github.com/en/rest/branches/branches#list-branches) |
| [List Commits](actions/list-commits.md) | `GET /repos/:owner/:repo/commits` | [docs](https://docs.github.com/en/rest/commits/commits#list-commits) |
| [List Pull Request Files](actions/list-pull-request-files.md) | `GET /repos/:owner/:repo/pulls/:pull_number/files` | [docs](https://docs.github.com/en/rest/pulls/pulls#list-pull-requests-files) |
| [List Pull Requests](actions/list-pull-requests.md) | `GET /repos/:owner/:repo/pulls` | [docs](https://docs.github.com/en/rest/pulls/pulls#list-pull-requests) |
| [List Releases](actions/list-releases.md) | `GET /repos/:owner/:repo/releases` | [docs](https://docs.github.com/en/rest/releases/releases#list-releases) |
| [List Repository Issues](actions/list-repository-issues.md) | `GET /repos/:owner/:repo/issues` | [docs](https://docs.github.com/en/rest/issues/issues#list-repository-issues) |
| [List Repository Workflow Runs](actions/list-repository-workflow-runs.md) | `GET /repos/:owner/:repo/actions/runs` | [docs](https://docs.github.com/en/rest/actions/workflow-runs#list-workflow-runs-for-a-repository) |
| [List Repository Workflows](actions/list-repository-workflows.md) | `GET /repos/:owner/:repo/actions/workflows` | [docs](https://docs.github.com/en/rest/actions/workflows#list-repository-workflows) |
| [Merge Pull Request](actions/merge-pull-request.md) | `PUT /repos/:owner/:repo/pulls/:pull_number/merge` | [docs](https://docs.github.com/en/rest/pulls/pulls#merge-a-pull-request) |
| [Search Issues and Pull Requests](actions/search-issues-and-pull-requests.md) | `GET /search/issues` | [docs](https://docs.github.com/en/rest/search/search?apiVersion=2022-11-28#search-issues-and-pull-requests) |
| [Search Repositories](actions/search-repositories.md) | `GET /search/repositories` | [docs](https://docs.github.com/en/rest/search/search?apiVersion=2022-11-28#search-repositories) |
| [Update Issue](actions/update-issue.md) | `PATCH /repos/:owner/:repo/issues/:issue_number` | [docs](https://docs.github.com/en/rest/issues/issues#update-an-issue) |
| [Update Pull Request](actions/update-pull-request.md) | `PATCH /repos/:owner/:repo/pulls/:pull_number` | [docs](https://docs.github.com/en/rest/pulls/pulls#update-a-pull-request) |
