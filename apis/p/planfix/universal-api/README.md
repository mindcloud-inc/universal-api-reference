# <img src="https://images.mindcloud.co/apps/icons/images-17_1774635245179.png" alt="Planfix logo" width="28" height="28"> Planfix: Universal API

Manage Planfix tasks, projects, contacts, and employees

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/planfix/latest
- **Category:** Productivity / Project Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://planfix.com
- **Vendor API docs:** https://help.planfix.com/restapidocs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Comment](actions/add-task-comment.md) | POST | Creates a new task comment in Planfix. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes a comment from Planfix. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Planfix. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves comments for a task in Planfix. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact or company in Planfix. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact or company from Planfix. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts and companies from Planfix. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact or company in Planfix. |

### Contact Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Filters](actions/list-contact-filters.md) | GET | Retrieves contact filters from Planfix. |

### Contact Template

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Templates](actions/list-contact-templates.md) | GET | Retrieves contact and company templates from Planfix. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from Planfix. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from Planfix. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Planfix. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Planfix. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Planfix. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Planfix. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Planfix. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Planfix. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Planfix. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Planfix. |

### Task Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Task Filters](actions/list-task-filters.md) | GET | Retrieves task filters from Planfix. |

