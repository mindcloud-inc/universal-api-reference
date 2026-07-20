# <img src="https://images.mindcloud.co/apps/icons/svgexport-1-1_1777384773332.png" alt="ClickUp logo" width="28" height="28"> ClickUp: Universal API

Manage projects, track tasks, chat with teams, and automate work.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clickUp/latest
- **Category:** Support / Ticketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clickup.com
- **Vendor API docs:** https://developer.clickup.com/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Authorized Workspaces](actions/list-authorized-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-authorized-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Attachment](actions/create-task-attachment.md) | POST |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List List Custom Fields](actions/list-list-custom-fields.md) | GET | View the Custom Fields in a specific List. |

### Custom Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Remove Custom Field Value](actions/remove-custom-field-value.md) | DELETE | Remove data from a Custom field on a task. |
| [Set Custom Field Value](actions/set-custom-field-value.md) | PUT | Add data to a Custom field on a task. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Search Workspace Docs](actions/search-workspace-docs.md) | GET |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | View the Folders in a Space. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Create List From Template](actions/create-list-from-template.md) | POST |  |
| [Get List](actions/get-list.md) | GET |  |
| [List Folderless Lists](actions/list-folderless-lists.md) | GET | View the Lists without a Folder |
| [List Lists](actions/list-lists.md) | GET | View the Lists within a Folder. |

### Task Template

| Action | Method | Description |
| --- | --- | --- |
| [List Task Templates](actions/list-task-templates.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Create a new task. |
| [Create Task From Template](actions/create-task-from-template.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE | Delete a task from Workspace. |
| [Get Task](actions/get-task.md) | GET |  |
| [List Filtered Team Tasks](actions/list-filtered-team-tasks.md) | GET | View the tasks that meet specific criteria from a Workspace. |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Authorized Workspaces](actions/list-authorized-workspaces.md) | GET | View the Workspaces available to the authenticated user. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Create List View](actions/create-list-view.md) | POST |  |
| [Get View Tasks](actions/get-view-tasks.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET | View the Spaces available in a Workspace. |

