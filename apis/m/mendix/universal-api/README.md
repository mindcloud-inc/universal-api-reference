# <img src="https://images.mindcloud.co/apps/icons/mendix_1776800649637.png" alt="Mendix logo" width="28" height="28"> Mendix: Universal API

Mendix is a low-code application development and deployment platform. This connector wraps Mendix Platform APIs for managing projects, apps, repository metadata, epics, feedback, catalog assets, webhooks, categories, and related operational resources through PAT-authenticated API calls.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mendix/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mendix.com/
- **Vendor API docs:** https://docs.mendix.com/apidocs-mxsdk/apidocs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Creation Job](actions/get-project-creation-job.md) | GET | Retrieves a project creation job status from Mendix. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Mendix and returns a job. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Mendix. |
| [Get Project](actions/get-project.md) | GET | Retrieves full project details from Mendix. |
| [List Account Projects](actions/list-account-projects.md) | GET | Retrieves company-owned projects for an account in Mendix. |
| [List Projects](actions/list-projects.md) | GET | Retrieves company-owned projects from Mendix. |
| [List User Projects](actions/list-user-projects.md) | GET | Retrieves a user's project memberships from Mendix. |
| [Update Project Categories](actions/update-project-categories.md) | PUT | Updates project category assignments in Mendix. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Role](actions/get-project-role.md) | GET | Retrieves a project role from Mendix. |
| [List Account Project Roles](actions/list-account-project-roles.md) | GET | Retrieves project roles for an account in Mendix. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Member](actions/add-project-member.md) | POST | Adds a project team member in Mendix or sends an invitation. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project team members from Mendix. |
| [Remove Project Member](actions/remove-project-member.md) | DELETE | Removes a project team member from Mendix. |
| [Update Project Member](actions/update-project-member.md) | PUT | Updates a project team member in Mendix. |

