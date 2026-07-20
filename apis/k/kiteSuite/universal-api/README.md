# <img src="https://images.mindcloud.co/apps/icons/kite-suite_1775491325172.png" alt="KiteSuite logo" width="28" height="28"> KiteSuite: Universal API

Plan projects, track tasks, collaborate, and automate workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kiteSuite/latest
- **Category:** Productivity / Project Management
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kitesuite.com/
- **Vendor API docs:** https://api.kitesuite.com/swagger/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspace Roles](actions/list-workspace-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Documents](actions/list-workspace-documents.md) | GET | Retrieves workspace documents from KiteSuite. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in KiteSuite. |
| [List Project Lists](actions/list-project-lists.md) | GET | Retrieves a list from KiteSuite by list ID. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in KiteSuite. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in KiteSuite. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from KiteSuite. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from KiteSuite. |
| [Get Project Data](actions/get-project-data.md) | GET | Retrieves all project data from KiteSuite. |
| [Get Workspace Project Data](actions/get-workspace-project-data.md) | GET | Retrieves projects, lists, sprints, and epics for a workspace in KiteSuite. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in KiteSuite. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Roles](actions/list-workspace-roles.md) | GET | Retrieves workspace roles from KiteSuite. |
| [Update Workspace Role](actions/update-workspace-role.md) | PUT | Updates an existing workspace role in KiteSuite. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Move Task To List](actions/move-task-to-list.md) | PUT | Moves a task to another list in KiteSuite. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Member](actions/add-project-member.md) | POST | Adds a member to a project in KiteSuite. |
| [Add Workspace Member](actions/add-workspace-member.md) | POST | Adds a member to a workspace in KiteSuite. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from KiteSuite. |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Retrieves workspace users from KiteSuite. |
| [Update Project Member Role](actions/update-project-member-role.md) | PUT | Updates a project member role in KiteSuite. |
| [Update Workspace Member Role](actions/update-workspace-member-role.md) | PUT | Updates a workspace member role in KiteSuite. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from KiteSuite. |
| [List User Workspaces](actions/list-user-workspaces.md) | GET | Retrieves a user's workspaces from KiteSuite. |
| [Search Workspace Data](actions/search-workspace-data.md) | GET | Finds workspace data in KiteSuite by search query. |

