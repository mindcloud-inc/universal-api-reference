# <img src="https://images.mindcloud.co/apps/icons/wrike_1773265933598.png" alt="Wrike logo" width="28" height="28"> Wrike: Universal API

Wrike: Manage tasks, projects, and collaborative work management data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wrike/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wrike.com
- **Vendor API docs:** https://developers.wrike.com/overview/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Access URL for Attachment](actions/get-access-url-for-attachment.md) | GET | Retrieves an access URL for a Wrike attachment. |
| [List Attachments](actions/list-attachments.md) | GET | Finds attachments in Wrike. |
| [List Task Attachments](actions/list-task-attachments.md) | GET | Finds attachments on a Wrike task. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Comment](actions/create-task-comment.md) | POST | Creates a new comment on a Wrike task. |
| [List Comments](actions/list-comments.md) | GET | Finds comments in Wrike. |
| [List Task Comments](actions/list-task-comments.md) | GET | Finds comments on a Wrike task. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Wrike. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Finds contacts in Wrike. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Finds custom fields in Wrike. |

### Dependency

| Action | Method | Description |
| --- | --- | --- |
| [List Task Dependencies](actions/list-task-dependencies.md) | GET | Finds dependencies for a Wrike task. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in a Wrike folder. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Wrike. |
| [List Folder Children](actions/list-folder-children.md) | GET | Finds child folders in a Wrike folder. |
| [List Folders](actions/list-folders.md) | GET | Finds folders in Wrike. |
| [List Space Folders](actions/list-space-folders.md) | GET | Finds folders in a Wrike space. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Wrike. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves a space from Wrike by ID. |
| [List Spaces](actions/list-spaces.md) | GET | Finds spaces in Wrike. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in a Wrike folder. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Wrike. |
| [List Folder Tasks](actions/list-folder-tasks.md) | GET | Finds tasks in a Wrike folder. |
| [List Space Tasks](actions/list-space-tasks.md) | GET | Finds tasks in a Wrike space. |
| [List Tasks](actions/list-tasks.md) | GET | Finds tasks in Wrike. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Wrike. |

