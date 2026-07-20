# <img src="https://images.mindcloud.co/apps/icons/git-hub-1772812242447_1777566970607.png" alt="GitHub Utils logo" width="28" height="28"> GitHub Utils: Universal API

GitHub Utils provides utility actions for repositories, issues, pull requests, commits, files, releases, and workflow runs through the GitHub REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gitHubUtils/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com
- **Vendor API docs:** https://docs.github.com/en/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from a GitHub repository. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue Comment](actions/create-issue-comment.md) | POST | Creates an issue comment on GitHub. |

### Commit

| Action | Method | Description |
| --- | --- | --- |
| [List Commits](actions/list-commits.md) | GET | Retrieves commits from a GitHub repository. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository Content](actions/get-repository-content.md) | GET | Retrieves repository content from GitHub. |
| [List Pull Request Files](actions/list-pull-request-files.md) | GET | Retrieves files from a GitHub pull request. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue on GitHub. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from a GitHub repository. |
| [List Repository Issues](actions/list-repository-issues.md) | GET | Retrieves issues from a GitHub repository. |
| [Search Issues and Pull Requests](actions/search-issues-and-pull-requests.md) | GET | Finds issues and pull requests on GitHub by query. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue on GitHub. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Authenticated User Organizations](actions/list-authenticated-user-organizations.md) | GET | Retrieves organizations for the authenticated GitHub user. |

### Pull Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Pull Request](actions/create-pull-request.md) | POST | Creates a pull request on GitHub. |
| [Get Pull Request](actions/get-pull-request.md) | GET | Retrieves a pull request from a GitHub repository. |
| [List Pull Requests](actions/list-pull-requests.md) | GET | Retrieves pull requests from a GitHub repository. |
| [Update Pull Request](actions/update-pull-request.md) | PUT | Updates an existing pull request on GitHub. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Release](actions/get-latest-release.md) | GET | Retrieves the latest release from a GitHub repository. |
| [List Releases](actions/list-releases.md) | GET | Retrieves releases from a GitHub repository. |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository](actions/get-repository.md) | GET | Retrieves a repository from GitHub. |
| [List Authenticated User Repositories](actions/list-authenticated-user-repositories.md) | GET | Retrieves repositories for the authenticated GitHub user. |
| [Search Repositories](actions/search-repositories.md) | GET | Finds repositories on GitHub by query. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from GitHub. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [List Repository Workflows](actions/list-repository-workflows.md) | GET | Retrieves workflows from a GitHub repository. |

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Run](actions/get-workflow-run.md) | GET | Retrieves a workflow run from a GitHub repository. |
| [List Repository Workflow Runs](actions/list-repository-workflow-runs.md) | GET | Retrieves workflow runs from a GitHub repository. |

