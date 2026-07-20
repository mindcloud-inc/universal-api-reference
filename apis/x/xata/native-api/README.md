# Xata: Native API Reference

A consolidated summary of Xata's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://xata.io/docs/api-reference/organizations/get-list-of-organizations
- **OpenAPI specification:** https://api.xata.tech/openapi.json
- **API base URL:** `https://api.xata.tech`

## Authentication

### Xata API Key

Use a Xata API key. MindCloud sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://xata.io/docs/platform/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Retrieve branch logs](actions/branch-logs.md) | `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/logs` | [docs](https://xata.io/docs/api-reference/branches/retrieve-branch-logs) |
| [Retrieve branch metrics](actions/branch-metrics.md) | `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/metrics` | [docs](https://xata.io/docs/api-reference/branches/retrieve-branch-metrics) |
| [Create a new branch](actions/create-branch.md) | `POST /organizations/:organizationID/projects/:projectID/branches` | [docs](https://xata.io/docs/api-reference/branches/create-a-new-branch) |
| [Create GitHub App installation](actions/create-github-app-installation.md) | `POST /organizations/:organizationID/githubapp/installations` | [docs](https://xata.io/docs/api-reference/github-app/create-github-app-installation) |
| [Create GitHub repository mapping](actions/create-github-repository.md) | `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository` | [docs](https://xata.io/docs/api-reference/github-app/create-github-repository-mapping) |
| [Create an Organization API Key](actions/create-organization-api-key.md) | `POST /organizations/:organizationID/api-keys` | [docs](https://xata.io/docs/api-reference/api-keys/create-an-organization-api-key) |
| [Send an invitation to join an organization](actions/create-organization-invitation.md) | `POST /organizations/:organizationID/invitations` | [docs](https://xata.io/docs/api-reference/organizations/send-an-invitation-to-join-an-organization) |
| [Create a new project](actions/create-project.md) | `POST /organizations/:organizationID/projects` | [docs](https://xata.io/docs/api-reference/projects/create-a-new-project) |
| [Create a User API Key](actions/create-user-api-key.md) | `POST /api-keys` | [docs](https://xata.io/docs/api-reference/api-keys/create-a-user-api-key) |
| [Delete a branch](actions/delete-branch.md) | `DELETE /organizations/:organizationID/projects/:projectID/branches/:branchID` | [docs](https://xata.io/docs/api-reference/branches/delete-a-branch) |
| [Delete GitHub repository mapping](actions/delete-github-repository.md) | `DELETE /organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository` | [docs](https://xata.io/docs/api-reference/github-app/delete-github-repository-mapping) |
| [Bulk delete API Keys for an organization](actions/delete-organization-api-keys.md) | `DELETE /organizations/:organizationID/api-keys` | [docs](https://xata.io/docs/api-reference/api-keys/bulk-delete-api-keys-for-an-organization) |
| [Delete an invitation](actions/delete-organization-invitation.md) | `DELETE /organizations/:organizationID/invitations/:invitationID` | [docs](https://xata.io/docs/api-reference/organizations/delete-an-invitation) |
| [Delete a project](actions/delete-project.md) | `DELETE /organizations/:organizationID/projects/:projectID` | [docs](https://xata.io/docs/api-reference/projects/delete-a-project) |
| [Bulk delete API Keys for the authenticated user](actions/delete-user-api-keys.md) | `DELETE /api-keys` | [docs](https://xata.io/docs/api-reference/api-keys/bulk-delete-api-keys-for-the-authenticated-user) |
| [Get branch details](actions/describe-branch.md) | `GET /organizations/:organizationID/projects/:projectID/branches/:branchID` | [docs](https://xata.io/docs/api-reference/branches/get-branch-details) |
| [Get project backup by ID](actions/get-backup.md) | `GET /organizations/:organizationID/projects/:projectID/backups/:backupID` | [docs](https://xata.io/docs/api-reference/projects/get-project-backup-by-id) |
| [Retrieve branch credentials](actions/get-branch-credentials.md) | `GET /organizations/:organizationID/projects/:projectID/branches/:branchID/credentials` | [docs](https://xata.io/docs/api-reference/branches/retrieve-branch-credentials) |
| [Get PostgreSQL configuration details](actions/get-branch-postgres-config.md) | `GET /organizations/:organizationID/projects/:projectID/branches/:branchID/postgres-config` | [docs](https://xata.io/docs/api-reference/branches/get-postgresql-configuration-details) |
| [Get project resource limits](actions/get-default-project-limits.md) | `GET /organizations/:organizationID/projects/limits` | [docs](https://xata.io/docs/api-reference/projects/get-project-resource-limits) |
| [Get GitHub repository for branch](actions/get-github-repository.md) | `GET /organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository` | [docs](https://xata.io/docs/api-reference/github-app/get-github-repository-for-branch) |
| [Get organization details](actions/get-organization.md) | `GET /organizations/:organizationID` | [docs](https://xata.io/docs/api-reference/organizations/get-organization-details) |
| [Get details of a specific invitation](actions/get-organization-invitation.md) | `GET /organizations/:organizationID/invitations/:invitationID` | [docs](https://xata.io/docs/api-reference/organizations/get-details-of-a-specific-invitation) |
| [Get list of organizations](actions/get-organizations-list.md) | `GET /organizations` | [docs](https://xata.io/docs/api-reference/organizations/get-list-of-organizations) |
| [Get project details](actions/get-project.md) | `GET /organizations/:organizationID/projects/:projectID` | [docs](https://xata.io/docs/api-reference/projects/get-project-details) |
| [List project backups](actions/list-backups.md) | `GET /organizations/:organizationID/projects/:projectID/backups` | [docs](https://xata.io/docs/api-reference/projects/list-project-backups) |
| [List all branches](actions/list-branches.md) | `GET /organizations/:organizationID/projects/:projectID/branches` | [docs](https://xata.io/docs/api-reference/branches/list-all-branches) |
| [Get available extensions for image](actions/list-extensions.md) | `GET /organizations/:organizationID/extensions` | [docs](https://xata.io/docs/api-reference/projects/get-available-extensions-for-image) |
| [List GitHub App installations for organization](actions/list-github-app-installations.md) | `GET /organizations/:organizationID/githubapp/installations` | [docs](https://xata.io/docs/api-reference/github-app/list-github-app-installations-for-organization) |
| [Get available images](actions/list-images.md) | `GET /organizations/:organizationID/images` | [docs](https://xata.io/docs/api-reference/projects/get-available-images) |
| [Get available instance types](actions/list-instance-types.md) | `GET /organizations/:organizationID/instanceTypes` | [docs](https://xata.io/docs/api-reference/projects/get-available-instance-types) |
| [List API Keys for an organization](actions/list-organization-api-keys.md) | `GET /organizations/:organizationID/api-keys` | [docs](https://xata.io/docs/api-reference/api-keys/list-api-keys-for-an-organization) |
| [List invitations for an organization](actions/list-organization-invitations.md) | `GET /organizations/:organizationID/invitations` | [docs](https://xata.io/docs/api-reference/organizations/list-invitations-for-an-organization) |
| [List members of an organization](actions/list-organization-members.md) | `GET /organizations/:organizationID/members` | [docs](https://xata.io/docs/api-reference/organizations/list-members-of-an-organization) |
| [List all projects](actions/list-projects.md) | `GET /organizations/:organizationID/projects` | [docs](https://xata.io/docs/api-reference/projects/list-all-projects) |
| [Get available regions](actions/list-regions.md) | `GET /organizations/:organizationID/regions` | [docs](https://xata.io/docs/api-reference/projects/get-available-regions) |
| [List API Keys for the authenticated user](actions/list-user-api-keys.md) | `GET /api-keys` | [docs](https://xata.io/docs/api-reference/api-keys/list-api-keys-for-the-authenticated-user) |
| [Execute SQL query](actions/query.md) | `POST /sql` | [docs](https://xata.io/docs/api-reference/gateway/execute-sql-query) |
| [Resend an invitation](actions/resend-organization-invitation.md) | `POST /organizations/:organizationID/invitations/:invitationID/resend` | [docs](https://xata.io/docs/api-reference/organizations/resend-an-invitation) |
| [Create a new branch from a backup of another branch](actions/restore-from-backup.md) | `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/restore` | [docs](https://xata.io/docs/api-reference/branches/create-a-new-branch-from-a-backup-of-another-branch) |
| [Rotate branch credentials](actions/rotate-branch-credentials.md) | `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/credentials/rotate` | [docs](https://xata.io/docs/api-reference/branches/rotate-branch-credentials) |
| [Update branch details](actions/update-branch.md) | `PATCH /organizations/:organizationID/projects/:projectID/branches/:branchID` | [docs](https://xata.io/docs/api-reference/branches/update-branch-details) |
| [Update GitHub App installation](actions/update-github-app-installation.md) | `PUT /organizations/:organizationID/githubapp/installations/:githubInstallationID` | [docs](https://xata.io/docs/api-reference/github-app/update-github-app-installation) |
| [Update GitHub repository mapping](actions/update-github-repository.md) | `PUT /organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository` | [docs](https://xata.io/docs/api-reference/github-app/update-github-repository-mapping) |
| [Update project details](actions/update-project.md) | `PATCH /organizations/:organizationID/projects/:projectID` | [docs](https://xata.io/docs/api-reference/projects/update-project-details) |
