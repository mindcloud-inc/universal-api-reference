# <img src="https://images.mindcloud.co/apps/icons/bitbucket-icon-square_1775749976130.png" alt="Bitbucket logo" width="28" height="28"> Bitbucket: Universal API

Bitbucket Cloud is Atlassian's Git repository hosting and collaboration platform for repositories, pull requests, pipelines, projects, snippets, and workspace administration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bitbucket/latest
- **Actions:** 52
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bitbucket.org/
- **Vendor API docs:** https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace](actions/get-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspace=mindcloudbitbucket20260409" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (52)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Pull Request Activity](actions/list-pull-request-activity.md) | GET | Retrieves pull request activity from Bitbucket. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Download Artifact Link](actions/get-download-artifact-link.md) | GET | Retrieves a download artifact link from Bitbucket. |
| [List Repository Downloads](actions/list-repository-downloads.md) | GET | Retrieves repository download artifacts from Bitbucket. |

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Get Branch](actions/get-branch.md) | GET | Retrieves a branch from Bitbucket. |
| [List Branches](actions/list-branches.md) | GET | Retrieves open branches from Bitbucket. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Commit Comment](actions/get-commit-comment.md) | GET | Retrieves a commit comment from Bitbucket. |
| [Get Pull Request Comment](actions/get-pull-request-comment.md) | GET | Retrieves a pull request comment from Bitbucket. |
| [List Commit Comments](actions/list-commit-comments.md) | GET | Retrieves commit comments from Bitbucket. |
| [List Pull Request Comments](actions/list-pull-request-comments.md) | GET | Retrieves pull request comments from Bitbucket. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Snippet Comment](actions/get-snippet-comment.md) | GET | Retrieves a snippet comment from Bitbucket. |
| [List Snippet Comments](actions/list-snippet-comments.md) | GET | Retrieves snippet comments from Bitbucket. |

### Commit

| Action | Method | Description |
| --- | --- | --- |
| [Get Commit](actions/get-commit.md) | GET | Retrieves a commit from Bitbucket. |
| [List Commits](actions/list-commits.md) | GET | Retrieves commits from Bitbucket. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Snippet](actions/get-snippet.md) | GET | Retrieves a snippet from Bitbucket. |
| [List Snippets in Workspace](actions/list-snippets-in-workspace.md) | GET | Retrieves snippets from a Bitbucket workspace. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline from Bitbucket. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Bitbucket. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Bitbucket. |
| [List Projects in Workspace](actions/list-projects-in-workspace.md) | GET | Retrieves projects from a Bitbucket workspace. |

### Pull Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Pull Request](actions/get-pull-request.md) | GET | Retrieves a pull request from Bitbucket. |
| [List Pull Requests](actions/list-pull-requests.md) | GET | Retrieves pull requests from Bitbucket. |

### Repositories

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Repository](actions/create-or-update-repository.md) | POST | Creates or updates a repository in Bitbucket. |
| [Delete Repository](actions/delete-repository.md) | DELETE | Deletes a repository from Bitbucket. |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository](actions/get-repository.md) | GET | Retrieves a repository from Bitbucket. |
| [List Repositories in Workspace](actions/list-repositories-in-workspace.md) | GET | Retrieves repositories from a Bitbucket workspace. |
| [List Repository Forks](actions/list-repository-forks.md) | GET | Retrieves repository forks from Bitbucket. |

### Repository Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Repository Permissions](actions/list-workspace-repository-permissions.md) | GET | Retrieves workspace repository permissions from Bitbucket. |

### Repository Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository Settings Inheritance](actions/get-repository-settings-inheritance.md) | GET | Retrieves repository settings inheritance from Bitbucket. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Pull Request Statuses](actions/list-pull-request-statuses.md) | GET | Retrieves pull request commit statuses from Bitbucket. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Bitbucket. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Bitbucket. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Pull Request Task](actions/get-pull-request-task.md) | GET | Retrieves a pull request task from Bitbucket. |
| [List Pull Request Tasks](actions/list-pull-request-tasks.md) | GET | Retrieves pull request tasks from Bitbucket. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Check Snippet Watching](actions/check-snippet-watching.md) | GET | Retrieves current snippet watch status from Bitbucket. |
| [Get Branch Restriction Rule](actions/get-branch-restriction-rule.md) | GET | Retrieves a branch restriction rule from Bitbucket. |
| [Get Effective Branching Model](actions/get-effective-branching-model.md) | GET | Retrieves the effective branching model from Bitbucket. |
| [Get Repository Branching Model](actions/get-repository-branching-model.md) | GET | Retrieves a repository branching model from Bitbucket. |
| [Get Repository Branching Model Settings](actions/get-repository-branching-model-settings.md) | GET | Retrieves repository branching model settings from Bitbucket. |
| [Get Repository Deploy Key](actions/get-repository-deploy-key.md) | GET | Retrieves a repository deploy key from Bitbucket. |
| [List Branch Restrictions](actions/list-branch-restrictions.md) | GET | Retrieves branch restrictions from Bitbucket. |
| [List Repository Deploy Keys](actions/list-repository-deploy-keys.md) | GET | Retrieves repository deploy keys from Bitbucket. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Member](actions/get-workspace-member.md) | GET | Retrieves a workspace member from Bitbucket. |
| [List Project Default Reviewers](actions/list-project-default-reviewers.md) | GET | Retrieves project default reviewers from Bitbucket. |
| [List Repository Watchers](actions/list-repository-watchers.md) | GET | Retrieves repository watchers from Bitbucket. |
| [List Workspace Members](actions/list-workspace-members.md) | GET | Retrieves workspace members from Bitbucket. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Snippet Watchers](actions/list-snippet-watchers.md) | GET | Retrieves snippet watchers from Bitbucket. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository Webhook](actions/get-repository-webhook.md) | GET | Retrieves a repository webhook from Bitbucket. |
| [List Repository Webhooks](actions/list-repository-webhooks.md) | GET | Retrieves repository webhooks from Bitbucket. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Bitbucket. |
| [List My Workspaces](actions/list-my-workspaces.md) | GET | Retrieves your Bitbucket workspaces. |

### Workspace Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get User Workspace Permission](actions/get-user-workspace-permission.md) | GET | Retrieves your workspace permission from Bitbucket. |
| [List Workspace Permissions](actions/list-workspace-permissions.md) | GET | Retrieves workspace permissions from Bitbucket. |

