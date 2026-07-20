# <img src="https://images.mindcloud.co/apps/icons/e3236af1-c400-48ae-87d8-8a6cc2fafb1a-2_1776092847800.png" alt="Scaleway logo" width="28" height="28"> Scaleway: Universal API

Scaleway is a cloud infrastructure platform for managing projects and other cloud resources through the Scaleway API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scaleway/latest
- **Category:** IT Operations / DevOps
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scaleway.com/
- **Vendor API docs:** https://www.scaleway.com/en/developers/api/account/project-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/list-projects?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | POST | Creates a new application in Scaleway. |
| [Delete Application](actions/delete-application.md) | DELETE | Deletes an existing application from Scaleway. |
| [Get Application](actions/get-application.md) | GET | Retrieves an application from Scaleway. |
| [List Applications](actions/list-applications.md) | GET | Retrieves applications from Scaleway for an organization. |
| [Update Application](actions/update-application.md) | PUT | Updates an existing application in Scaleway. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Scaleway. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Scaleway. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Scaleway. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Scaleway for an organization. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Scaleway. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Scaleway. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Scaleway. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Scaleway. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Scaleway for an organization. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Scaleway. |

### Ssh Key

| Action | Method | Description |
| --- | --- | --- |
| [Create SSH Key](actions/create-ssh-key.md) | POST | Creates a new SSH key in Scaleway. |
| [Delete SSH Key](actions/delete-ssh-key.md) | DELETE | Deletes an existing SSH key from Scaleway. |
| [Get SSH Key](actions/get-ssh-key.md) | GET | Retrieves an SSH key from Scaleway. |
| [List SSH Keys](actions/list-ssh-keys.md) | GET | Retrieves SSH keys from Scaleway for a project. |
| [Update SSH Key](actions/update-ssh-key.md) | PUT | Updates an existing SSH key in Scaleway. |

