# <img src="https://images.mindcloud.co/apps/icons/9c44412a-238d-4bdb-96bc-95edca4af4b7-5_1777051782498.png" alt="Infisical logo" width="28" height="28"> Infisical: Universal API

Manage secrets, certificates, and secure infrastructure access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/infisical/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://infisical.com
- **Vendor API docs:** https://infisical.com/docs/api-reference/overview/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Folder By ID](actions/get-folder-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/get-folder-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in an Infisical project. |
| [Delete Environment](actions/delete-environment.md) | DELETE | Deletes an existing environment from an Infisical project. |
| [Update Environment](actions/update-environment.md) | PUT | Updates an existing environment in an Infisical project. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in an Infisical environment. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Infisical by ID or name. |
| [Get Folder By ID](actions/get-folder-by-id.md) | GET | Retrieves a folder from Infisical by ID. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from a project environment in Infisical. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST | Authenticates with Infisical using Universal Auth. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Infisical. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Infisical. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Infisical by ID. |
| [Get Project By Slug](actions/get-project-by-slug.md) | GET | Retrieves a project from Infisical by slug. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Infisical. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Infisical. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Create Secret](actions/create-secret.md) | POST | Creates a new secret in a project environment in Infisical. |
| [Delete Secret](actions/delete-secret.md) | DELETE | Deletes an existing secret from a project environment in Infisical. |
| [List Secrets](actions/list-secrets.md) | GET | Retrieves secrets from a project environment in Infisical. |
| [Retrieve Secret](actions/retrieve-secret.md) | GET | Retrieves a secret from a project environment in Infisical. |
| [Update Secret](actions/update-secret.md) | PUT | Updates an existing secret in a project environment in Infisical. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag for a project in Infisical. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags for a project in Infisical. |

