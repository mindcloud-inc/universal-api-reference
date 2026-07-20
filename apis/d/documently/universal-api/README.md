# <img src="https://images.mindcloud.co/apps/icons/documently-icon_1775485918609.png" alt="Documently logo" width="28" height="28"> Documently: Universal API

Documently is a documentation management platform for versioning, branching, publishing, file storage, team collaboration, API tokens, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documently/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://documently.io
- **Vendor API docs:** https://app.documently.io/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [List API Tokens](actions/list-api-tokens.md) | GET | Retrieves API tokens from Documently. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from Documently. |

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Create Branch](actions/create-branch.md) | POST | Creates a new branch in Documently. |
| [Delete Branch](actions/delete-branch.md) | DELETE | Deletes an existing branch from Documently. |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from Documently. |
| [Retrieve Branch](actions/retrieve-branch.md) | GET | Retrieves a branch from Documently. |
| [Update Branch](actions/update-branch.md) | PUT | Updates an existing branch in Documently. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Create Invitation](actions/create-invitation.md) | POST | Creates a new invitation in Documently. |
| [List Invitations](actions/list-invitations.md) | GET | Retrieves invitations from Documently. |
| [Retrieve Invitation](actions/retrieve-invitation.md) | GET | Retrieves an invitation from Documently. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Documently. |
| [Retrieve Organization](actions/retrieve-organization.md) | GET | Retrieves an organization from Documently. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Permissions](actions/list-permissions.md) | GET | Retrieves permissions from Documently. |
| [Retrieve Permission](actions/retrieve-permission.md) | GET | Retrieves a permission from Documently. |
| [Update Permission](actions/update-permission.md) | PUT | Updates an existing permission in Documently. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Documently. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a project from Documently. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Documently. |

### Storage Directory

| Action | Method | Description |
| --- | --- | --- |
| [List Storage Directories](actions/list-storage-directories.md) | GET | Retrieves storage directories from Documently. |
| [Retrieve Storage Directory](actions/retrieve-storage-directory.md) | GET | Retrieves a storage directory from Documently. |
| [Update Storage Directory](actions/update-storage-directory.md) | PUT | Updates an existing storage directory in Documently. |

### Storage File

| Action | Method | Description |
| --- | --- | --- |
| [List Storage Files](actions/list-storage-files.md) | GET | Retrieves storage files from Documently. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Current User](actions/retrieve-current-user.md) | GET | Retrieves the current user from Documently. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from Documently. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Documently. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Documently. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Documently. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Documently. |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET | Retrieves a webhook from Documently. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Documently. |

### Webhook Log

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Logs](actions/list-webhook-logs.md) | GET | Retrieves webhook logs from Documently. |

