# Scaleway: Native API Reference

A consolidated summary of Scaleway's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.scaleway.com/en/developers/api/account/project-api/
- **OpenAPI specification:** https://www.scaleway.com/en/developers/static/scaleway.account.v3.ProjectApi.yml
- **API base URL:** `https://api.scaleway.com`

## Authentication

### API Key

Use the secret part of your Scaleway API key as the connection secret.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Auth-Token: <apiKey>
```

[Official authentication documentation](https://www.scaleway.com/en/developers/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | `POST /iam/v1alpha1/applications` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Create Group](actions/create-group.md) | `POST /iam/v1alpha1/groups` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Create Project](actions/create-project.md) | `POST /account/v3/projects` | [docs](https://www.scaleway.com/en/developers/api/account/project-api/) |
| [Create SSH Key](actions/create-ssh-key.md) | `POST /iam/v1alpha1/ssh-keys` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Delete Application](actions/delete-application.md) | `DELETE /iam/v1alpha1/applications/:application_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Delete Group](actions/delete-group.md) | `DELETE /iam/v1alpha1/groups/:group_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Delete Project](actions/delete-project.md) | `DELETE /account/v3/projects/:project_id` | [docs](https://www.scaleway.com/en/developers/api/account/project-api/) |
| [Delete SSH Key](actions/delete-ssh-key.md) | `DELETE /iam/v1alpha1/ssh-keys/:ssh_key_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Get Application](actions/get-application.md) | `GET /iam/v1alpha1/applications/:application_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Get Group](actions/get-group.md) | `GET /iam/v1alpha1/groups/:group_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Get Project](actions/get-project.md) | `GET /account/v3/projects/:project_id` | [docs](https://www.scaleway.com/en/developers/api/account/project-api/) |
| [Get SSH Key](actions/get-ssh-key.md) | `GET /iam/v1alpha1/ssh-keys/:ssh_key_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [List Applications](actions/list-applications.md) | `GET /iam/v1alpha1/applications` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [List Groups](actions/list-groups.md) | `GET /iam/v1alpha1/groups` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [List Projects](actions/list-projects.md) | `GET /account/v3/projects` | [docs](https://www.scaleway.com/en/developers/api/account/project-api/) |
| [List SSH Keys](actions/list-ssh-keys.md) | `GET /iam/v1alpha1/ssh-keys` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Update Application](actions/update-application.md) | `PATCH /iam/v1alpha1/applications/:application_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Update Group](actions/update-group.md) | `PATCH /iam/v1alpha1/groups/:group_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
| [Update Project](actions/update-project.md) | `PATCH /account/v3/projects/:project_id` | [docs](https://www.scaleway.com/en/developers/api/account/project-api/) |
| [Update SSH Key](actions/update-ssh-key.md) | `PATCH /iam/v1alpha1/ssh-keys/:ssh_key_id` | [docs](https://www.scaleway.com/en/developers/api/iam/) |
