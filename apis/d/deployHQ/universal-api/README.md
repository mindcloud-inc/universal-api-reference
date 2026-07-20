# <img src="https://images.mindcloud.co/apps/icons/deploy-hq_1776273913753.png" alt="DeployHQ logo" width="28" height="28"> DeployHQ: Universal API

DeployHQ automates deployments from Git repositories to servers, with API access for managing projects, deployments, servers, repositories, templates, and deployment configuration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deployHQ/latest
- **Category:** IT Operations / DevOps
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deployhq.com
- **Vendor API docs:** https://www.deployhq.com/support/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [List Repository Branches](actions/list-repository-branches.md) | GET | Retrieves repository branches from DeployHQ. |

### Commit

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Commits](actions/list-recent-commits.md) | GET | Retrieves recent repository commits from DeployHQ. |

### Deployment

| Action | Method | Description |
| --- | --- | --- |
| [Abort Deployment](actions/abort-deployment.md) | PUT | Aborts a running deployment in DeployHQ. |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a deployment from DeployHQ. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves deployments for a project from DeployHQ. |
| [Queue Deployment](actions/queue-deployment.md) | POST | Creates a deployment for a project in DeployHQ. |
| [Retry Deployment](actions/retry-deployment.md) | PUT | Retries an existing deployment in DeployHQ. |
| [Rollback Deployment](actions/rollback-deployment.md) | PUT | Rolls back a deployment in DeployHQ. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves project integrations from DeployHQ. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in DeployHQ. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from DeployHQ. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from DeployHQ. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all projects from DeployHQ. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in DeployHQ. |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Replace Repository](actions/create-or-replace-repository.md) | PUT | Creates or replaces the repository in DeployHQ. |
| [Get Repository](actions/get-repository.md) | GET | Retrieves the repository for a project from DeployHQ. |
| [Update Repository](actions/update-repository.md) | PUT | Updates the repository for a project in DeployHQ. |

### Revision

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Revision](actions/get-latest-revision.md) | GET | Retrieves the latest repository revision from DeployHQ. |

### Server

| Action | Method | Description |
| --- | --- | --- |
| [Create Server](actions/create-server.md) | POST | Creates a new server in DeployHQ. |
| [Delete Server](actions/delete-server.md) | DELETE | Deletes an existing server from DeployHQ. |
| [Get Server](actions/get-server.md) | GET | Retrieves a server from DeployHQ. |
| [List Servers](actions/list-servers.md) | GET | Retrieves all servers for a project from DeployHQ. |
| [Update Server](actions/update-server.md) | PUT | Updates an existing server in DeployHQ. |

### Test Access

| Action | Method | Description |
| --- | --- | --- |
| [Run Server Test Access](actions/run-server-test-access.md) | POST | Runs a server access test in DeployHQ. |

