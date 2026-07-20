# <img src="https://images.mindcloud.co/apps/icons/favicon-xata-io-48x48_1777484152800.png" alt="Xata logo" width="28" height="28"> Xata: Universal API

Xata is a PostgreSQL platform for instant database branching, projects, branches, credentials, metrics, GitHub mappings, and API key management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xata/latest
- **Category:** IT Operations / Database
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xata.io
- **Vendor API docs:** https://xata.io/docs/api-reference/organizations/get-list-of-organizations

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get list of organizations](actions/get-organizations-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organizations-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Apikey

| Action | Method | Description |
| --- | --- | --- |
| [Create an Organization API Key](actions/create-organization-api-key.md) | POST |  |
| [Create a User API Key](actions/create-user-api-key.md) | POST |  |
| [Bulk delete API Keys for an organization](actions/delete-organization-api-keys.md) | DELETE |  |
| [Bulk delete API Keys for the authenticated user](actions/delete-user-api-keys.md) | DELETE |  |
| [List API Keys for an organization](actions/list-organization-api-keys.md) | GET |  |
| [List API Keys for the authenticated user](actions/list-user-api-keys.md) | GET |  |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create GitHub App installation](actions/create-github-app-installation.md) | POST |  |
| [Create GitHub repository mapping](actions/create-github-repository.md) | POST |  |
| [Delete GitHub repository mapping](actions/delete-github-repository.md) | DELETE |  |
| [Get GitHub repository for branch](actions/get-github-repository.md) | GET |  |
| [List GitHub App installations for organization](actions/list-github-app-installations.md) | GET |  |
| [Update GitHub App installation](actions/update-github-app-installation.md) | PUT |  |
| [Update GitHub repository mapping](actions/update-github-repository.md) | PUT |  |

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve branch logs](actions/branch-logs.md) | POST |  |
| [Retrieve branch metrics](actions/branch-metrics.md) | POST |  |
| [Create a new branch](actions/create-branch.md) | POST |  |
| [Delete a branch](actions/delete-branch.md) | DELETE |  |
| [Get branch details](actions/describe-branch.md) | GET |  |
| [Retrieve branch credentials](actions/get-branch-credentials.md) | GET |  |
| [Get PostgreSQL configuration details](actions/get-branch-postgres-config.md) | GET |  |
| [List all branches](actions/list-branches.md) | GET |  |
| [Rotate branch credentials](actions/rotate-branch-credentials.md) | POST |  |
| [Update branch details](actions/update-branch.md) | PUT |  |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Send an invitation to join an organization](actions/create-organization-invitation.md) | POST |  |
| [Delete an invitation](actions/delete-organization-invitation.md) | DELETE |  |
| [Get details of a specific invitation](actions/get-organization-invitation.md) | GET |  |
| [List invitations for an organization](actions/list-organization-invitations.md) | GET |  |
| [Resend an invitation](actions/resend-organization-invitation.md) | POST |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get organization details](actions/get-organization.md) | GET |  |
| [Get list of organizations](actions/get-organizations-list.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create a new project](actions/create-project.md) | POST |  |
| [Delete a project](actions/delete-project.md) | DELETE |  |
| [Get project backup by ID](actions/get-backup.md) | GET |  |
| [Get project resource limits](actions/get-default-project-limits.md) | GET |  |
| [Get project details](actions/get-project.md) | GET |  |
| [List project backups](actions/list-backups.md) | GET |  |
| [Get available extensions for image](actions/list-extensions.md) | GET |  |
| [Get available images](actions/list-images.md) | GET |  |
| [Get available instance types](actions/list-instance-types.md) | GET |  |
| [List all projects](actions/list-projects.md) | GET |  |
| [Get available regions](actions/list-regions.md) | GET |  |
| [Create a new branch from a backup of another branch](actions/restore-from-backup.md) | POST |  |
| [Update project details](actions/update-project.md) | PUT |  |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Execute SQL query](actions/query.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List members of an organization](actions/list-organization-members.md) | GET |  |

