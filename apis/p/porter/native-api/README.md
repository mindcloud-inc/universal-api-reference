# Porter: Native API Reference

A consolidated summary of Porter's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.porter.run/standard/cli/command-reference/porter-project
- **API base URL:** `https://dashboard.porter.run`

## Authentication

### Deploy Token

Use a Porter deploy token (PORTER_TOKEN) for API and CLI access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.porter.run/cli/basic-usage)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /api/users/current` | [docs](https://docs.porter.run/cli/basic-usage) |
| [Get Project Details](actions/get-project-details.md) | `GET /api/projects/:projectId` | [docs](https://docs.porter.run/standard/cli/command-reference/porter-project) |
| [List Applications](actions/list-applications.md) | `GET /api/v2/projects/:projectId/apps` | [docs](https://docs.porter.run/standard/cli/command-reference/porter-app) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET /api/v2/projects/:projectId/audit-logs` | [docs](https://docs.porter.run/) |
| [List Build Settings](actions/list-build-settings.md) | `GET /api/v2/projects/:projectId/build-settings` | [docs](https://docs.porter.run/applications/deploy/builds) |
| [List Cloud Accounts](actions/list-cloud-accounts.md) | `GET /api/v2/projects/:projectId/clouds` | [docs](https://docs.porter.run/cloud-accounts/overview) |
| [List Clusters](actions/list-clusters.md) | `GET /api/v2/projects/:projectId/clusters` | [docs](https://docs.porter.run/standard/cli/command-reference/porter-cluster) |
| [List Environment Groups](actions/list-environment-groups.md) | `GET /api/v2/alpha/projects/:projectId/cloud-environment-groups` | [docs](https://docs.porter.run/applications/configure/environment-groups) |
| [List Job Runs](actions/list-job-runs.md) | `GET /api/v2/projects/:projectId/job_runs` | [docs](https://docs.porter.run/applications/configuration-as-code/services/job-service) |
| [List Migrations](actions/list-migrations.md) | `GET /api/v2/projects/:projectId/migrations` | [docs](https://docs.porter.run/) |
| [List Project Invites](actions/list-project-invites.md) | `GET /api/v2/projects/:projectId/invites` | [docs](https://docs.porter.run/security-and-compliance/role-based-access-control) |
| [List Project Members](actions/list-project-members.md) | `GET /api/v2/projects/:projectId/members` | [docs](https://docs.porter.run/security-and-compliance/role-based-access-control) |
| [List Projects](actions/list-projects.md) | `GET /api/v2/projects` | [docs](https://docs.porter.run/standard/cli/command-reference/porter-project) |
| [List Services](actions/list-services.md) | `GET /api/v2/projects/:projectId/services` | [docs](https://docs.porter.run/applications/deploy/configuring-application-services) |
