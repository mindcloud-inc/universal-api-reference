# <img src="https://images.mindcloud.co/apps/icons/git-hub_1772812242447.png" alt="GitHub logo" width="28" height="28"> GitHub: Universal API

GitHub is a developer platform for hosting code, reviewing changes, and automating software workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/github/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com
- **Vendor API docs:** https://docs.github.com/en/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Branches

| Action | Method | Description |
| --- | --- | --- |
| [List Branches](actions/list-branches.md) | GET | Lists branches in a GitHub repository. |

### Commits

| Action | Method | Description |
| --- | --- | --- |
| [List Commits](actions/list-commits.md) | GET | Lists commits in a GitHub repository. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository Content](actions/get-repository-content.md) | GET | Retrieves repository content from GitHub. |
| [List Pull Request Files](actions/list-pull-request-files.md) | GET | Lists files in a GitHub pull request. |

### Issue Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue Comment](actions/create-issue-comment.md) | POST | Creates an issue comment in GitHub. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates an issue in a GitHub repository. |
| [Create Pull Request](actions/create-pull-request.md) | POST | Creates a pull request in a GitHub repository. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from a GitHub repository. |
| [Get Pull Request](actions/get-pull-request.md) | GET | Retrieves a pull request from a GitHub repository. |
| [List Pull Requests](actions/list-pull-requests.md) | GET | Lists pull requests in a GitHub repository. |
| [List Repository Issues](actions/list-repository-issues.md) | GET | Lists issues in a GitHub repository. |
| [Merge Pull Request](actions/merge-pull-request.md) | PUT | Merges a pull request into the base branch in GitHub. |
| [Search Issues and Pull Requests](actions/search-issues-and-pull-requests.md) | GET | Finds GitHub issues and pull requests by search query. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an issue in a GitHub repository. |
| [Update Pull Request](actions/update-pull-request.md) | PUT | Updates a pull request in a GitHub repository. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Authenticated User Organizations](actions/list-authenticated-user-organizations.md) | GET | Lists GitHub organizations for the authenticated user. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Create Release](actions/create-release.md) | POST | Creates a release in a GitHub repository. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Release](actions/get-latest-release.md) | GET | Retrieves the latest published release from a GitHub repository. |
| [List Releases](actions/list-releases.md) | GET | Lists releases in a GitHub repository. |

### Repositories

| Action | Method | Description |
| --- | --- | --- |
| [Create Repository for Authenticated User](actions/create-repository-for-authenticated-user.md) | POST | Creates a repository for the authenticated GitHub user. |
| [Get Repository](actions/get-repository.md) | GET | Retrieves a repository from GitHub. |
| [List Authenticated User Repositories](actions/list-authenticated-user-repositories.md) | GET | Lists GitHub repositories for the authenticated user. |
| [Search Repositories](actions/search-repositories.md) | GET | Finds repositories in GitHub by search query. |

### Repository Content

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update File Content](actions/create-or-update-file-content.md) | PUT | Creates or updates a file in a GitHub repository. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from a GitHub repository. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from GitHub. |

### Workflow Dispatch

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Dispatch Event](actions/create-workflow-dispatch-event.md) | POST | Triggers a GitHub Actions workflow run. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Run](actions/get-workflow-run.md) | GET | Retrieves a workflow run from GitHub. |
| [List Repository Workflow Runs](actions/list-repository-workflow-runs.md) | GET | Lists workflow runs in a GitHub repository. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Repository Workflows](actions/list-repository-workflows.md) | GET | Lists workflows in a GitHub repository. |

